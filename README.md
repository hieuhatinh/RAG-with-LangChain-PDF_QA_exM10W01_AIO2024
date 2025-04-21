# Exercise M010W01 - RAG with LangChain for PDF Question Answering - AIO2024

**LangChain** là một framework được thiết kế chuyên biệt cho việc triển khai LLMs trong các ứng dụng thực tế. LangChain hỗ trợ các công cụ và thư viện mạnh mẽ cho phép các nhà phát triển dễ dàng tích hợp các mô hình ngôn ngữ lớn với các ứng dụng của họ, từ các Chatbot thông minh cho đến các hệ thống phân tích dữ liệu phức tạp.
![Minh họa ứng dụng hỏi đáp nội dung PDF sử dụng LangChain](/readme_image/illustration_app.png)

Bài tập này xây dựng một ứng dụng về RAG trả lời các câu hỏi học thuật tận dụng các bài báo khoa học mà ta thu thập được, sử dụng thư viện LangChain. Pipline như sau: 
![Pipeline](/readme_image/pipeline.png)


#### Tổng quan thư mục: 

![Folder Architecture](/readme_image/folder.png)
- **data_source/:** Thư mục dùng để lưu trữ các tài liệu phục vụ cho việc xây dựng hệ cơ sở dữ liệu vector
- **data_source/generative_ai/download.py:** File code dùng để tải tự động một số các
 bài báo khoa học dưới dạng file pdf.
- **src/base/llm_model:** File code dùng để khai báo hàm khởi tạo mô hình ngôn ngữ lớn
- **src/rag/:** Thư mục dùng để lưu trữ các code liên quan đến xây dựng RAG, bao gồm:
    1. **src/rag/file_loader.py:** File code dùng để khai báo các hàm load file pdf (vì tài liệu của chúng ta thu thập thuộc file pdf).
    2. **src/rag/main.py:** File code dùng để khai báo hàm khởi tạo chains.
    3. **src/rag/offline_rag.py:** File code dùng để khai báo PromptTemplate.
    4. **src/rag/utils.py:** File code dùng để khai báo hàm tách câu trả lời từ model.
    5. **src/rag/vectorstore.py:** File code dùng để khai báo hàm khởi tạo hệ cơ sở dữ liệu
    vector.
- **src/app.py:** File code dùng để khởi tạo API.
- **requirements.txt:** File code dùng để khai báo các thư viện cần thiết để sử dụng source code