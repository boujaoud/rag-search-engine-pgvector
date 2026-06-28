# rag-search-engine-pgvector

Un moteur de recherche sémantique basé sur RAG pour interroger des documents PDF.

## C’est quoi ce projet ?

Ce projet permet de poser des questions sur des fichiers PDF comme si on discutait avec eux.

Au lieu de chercher des mots-clés, il comprend le sens des phrases.

## Comment ça marche

1. Tu ajoutes un PDF  
2. Le texte est extrait  
3. Il est découpé en petits morceaux (chunks)  
4. Chaque chunk est transformé en vecteur (embedding)  
5. Les vecteurs sont stockés dans PostgreSQL avec pgvector  
6. Quand tu poses une question :
   - elle est transformée en vecteur
   - on cherche les chunks les plus proches
   - le modèle répond avec le contexte trouvé  

## Stack technique

- Python  
- PostgreSQL  
- pgvector  
- embeddings (OpenAI ou autre modèle)

## À quoi ça sert

- chercher dans des PDF sans lire tout le document  
- faire du Q&A sur de la documentation  
- construire une base de connaissances intelligente  

## Idée du système

PDF → texte → chunks → embeddings → base vectorielle → recherche → réponse  

## Note

Ce projet est un MVP d'un système RAG simple avec une base vectorielle.