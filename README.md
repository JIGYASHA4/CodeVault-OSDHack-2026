# CodeVault-OSDHack-2026
An Offline AI Coding Memory that automatically collects coding solutions from multiple platforms, explains them using a local LLM, organizes them, and creates an AI-searchable knowledge base.

## Overall Architecture of the project
                   Browser Extension

        ┌─────────────────────────────────────┐
        │  LeetCode                           │
        │  CodeChef                           │
        │  GeeksForGeeks                      │
        │  Codeforces                         │
        │  Unstop                             │
        └─────────────────────────────────────┘
                     │
                     ▼

          Detect Accepted Submission

                     │
                     ▼

        Save Code + Metadata Locally

                     │
                     ▼

       Local AI (Ollama / llama.cpp)

                     │

     ┌───────────────┼─────────────────┐
     │               │                 │
     ▼               ▼                 ▼

   Explain        Complexity           Tags

     ▼               ▼                 ▼

  Generate README

  Generate Notes

  Generate Flashcards

  Generate Interview Questions

  Generate Commit Message

                     │
                     ▼

          Local Vector Database

          (Chroma / FAISS)

                     │

     Chat with your solved questions

                     │
                     ▼

       Push to GitHub Repository
