This project demonstrates how to build a LangChain-powered pipeline that:
- Dynamically reads PDF documents.
- Splits them into manageable text chunks.
- Summarizes the content using an LLM.
- Generates multiple-choice questions (MCQs) with answers based on the summary.
Key Features
- Dynamic PDF Input: Users can provide any PDF file path, and the pipeline automatically loads and processes it.
- Chunk Splitting & Combining: Text is split into smaller chunks to avoid token limits, then combined for summarization.
- Runnable Chains: Uses LangChain’s RunnableLambda and RunnablePassthrough for modular, composable workflows.
- Summarization: Extracts key points from the document using ChatPromptTemplate + LLM.
- MCQ Generation: Automatically creates structured MCQs (with options a–d and correct answers) from the summary.
Tech Stack
- LangChain: For building modular pipelines (RunnableLambda, RunnablePassthrough, ChatPromptTemplate).
- OpenAI GPT Models: For summarization and question generation.
- PyPDFLoader: For reading PDF documents.
- RecursiveCharacterTextSplitter: For splitting text into chunks.
Workflow
- Input: User provides the PDF file path.
- PDF Processing: The document is loaded and split into chunks.
- Summarization Chain: Chunks are combined and summarized by the LLM.
- MCQ Chain: The summary is passed into another chain that generates MCQs.
- Output: The user receives a set of MCQs with answers.