NLP_RetrievalAugmentedGeneration
Overview
This project demonstrates a simple Retrieval-Augmented Generation (RAG) system using TF-IDF and cosine similarity. The system retrieves relevant information from a document corpus and uses that information to help answer user questions.

Files Included
main.py
corpus.txt
README.md
How the System Works
Loads text documents from the corpus.
Splits the corpus into paragraph-level documents.
Uses TF-IDF vectorization to create document vectors.
Converts user queries into vectors.
Computes cosine similarity scores between queries and documents.
Retrieves the most relevant documents.
Generates a grounded answer using the retrieved context.
Example Queries
Query 1
Question: What time does the library open?

Answer: The library is open from 8:00 AM to 8:00 PM Monday through Friday.

Query 2
Question: How many study rooms does the library have?

Answer: The library has 10 study rooms.

Query 3
Question: How much does printing cost?

Answer: Printing costs $0.10 per page.

Reflection
The version with retrieval performed better because it used information directly from the corpus instead of relying on a generic response. Retrieval helped answer questions about library hours, study rooms, and printing costs by finding relevant information from the documents.

Retrieval worked well when the information was clearly available in the corpus. It was less effective because the corpus was small and often returned the same document for multiple queries. Since there was only a limited amount of information available, retrieval could not show much distinction between documents.

The answers were generally correct because they were based on the text in the corpus. If incorrect information existed in the corpus, the system would return incorrect answers as well.

To improve the system, I would add more documents, use better document chunking, and connect the retrieval system to a larger language model that could generate more natural and detailed responses from the retrieved context.
