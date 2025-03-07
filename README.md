Getting Started with the .NET AI Chat 
The .NET AI Chat template is designed to help you quickly build an AI-powered chat application to start chatting with custom data. This initial release focuses on a Blazor-based web app, built using the Microsoft.Extensions.AI and Microsoft.Extensions.VectorData abstractions. The template uses the Retrieval Augmented Generation (RAG) pattern commonly used for chat applications.

Key Features and Configuration Options
Chat with Custom Data: The template allows you to create a chat-based UI that can interact with sample PDFs or your own data using the RAG pattern.
Local and Azure Integration: The template supports both a local vector store for prototyping and Azure AI Search for more advanced configurations.
Customizable Code: The generated code includes UI components for chat interactions, citation tracking, and follow-up suggestions. You can customize or remove these components as needed.
Data Ingestion: The template includes code for data ingestion, caching, and processing, allowing you to handle various data sources and formats.

Chatting with your own data
This template includes two sample PDF files and an example of data ingestion code to process the PDFs. This data ingestion code is flexible so that you swap out the sample PDFs. To chat with your own data, do the following:

If you have your project running, stop it.
Remove the sample PDF files from the /wwwroot/Data folder.
Add your own PDF files to the /wwwroot/Data folder.
Run the application again.
On startup of the app, the data ingestion code (located in /Services/Ingestion/DataIngestor.cs) will compare the contents of the Data folder; it will remove old files from the configured vector store and add new ones. Note: depending on how many files you have, and how big they are, you may run into quota and rate limits with your configured AI model provider. When you hit a limit, you may see an error message or experience long delays in the startup of the application. 
