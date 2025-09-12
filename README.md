​Smart Study Companion AI
​This project is a powerful, privacy-focused, browser-based learning tool that transforms study materials (PDFs, images, text) into interactive summaries and quizzes using the power of AI. It operates as a single, self-contained index.html file, requiring no backend or complex setup for basic operation.
​The application features a tiered access key system managed by a client-side admin panel, allowing for feature-gating and usage limits.
​✨ Core Features
​Single-File Application: The entire app is contained within index.html, making it incredibly portable and easy to deploy on any static hosting service.
​Robust File Handling: Supports PDFs, TXT files, JPG/PNG images, and ZIP archives.
​Intelligent On-Device Text Extraction:
​Uses pdf.js for standard PDFs.
​Seamlessly falls back to client-side OCR with Tesseract.js for scanned documents and images.
​AI-Powered Study Tools: Integrates with the Google Gemini API to provide:
​Document Summarization
​Multiple-Choice Question (MCQ) Generation
​Key Point Extraction
​Tiered Access System:
​App functionality is locked behind an access key system.
​Features and usage (file uploads, daily AI queries) are controlled by defined tiers (e.g., Free, Premium).
​Client-Side Admin Panel: A hidden admin panel allows a developer/owner to configure access tiers and generate new user keys directly in the browser.
​Privacy First: All file parsing and OCR happens locally. Files are never uploaded. Only the extracted text from a selected document is sent to the AI API upon user action.
​Modern UI/UX: Built with Tailwind CSS, featuring a responsive design, animations, and both Dark and Light themes.
​Persistent State: User library, access key, and usage data are stored in the browser's localStorage.
​🛠️ Tech Stack
​HTML/CSS/JavaScript: The core of the application.
​Tailwind CSS: For all styling, loaded via CDN.
​pdf.js: Client-side PDF rendering and text extraction.
​Tesseract.js: Client-side Optical Character Recognition (OCR).
​JSZip: Client-side ZIP file unpacking.
​Google Gemini API: The AI provider for all generative features.
​🚀 Deployment
​This application is designed for easy deployment on any static web hosting platform. A complete, step-by-step guide is available in the Developer_Manual.md file. The most common method is using GitHub Pages:
​Create a new GitHub repository.
​Upload the index.html file to the repository.
​Enable GitHub Pages in the repository's settings, deploying from the main branch.
​The application will be live at the provided GitHub Pages URL.
​⚠️ Important Note on the Admin Panel
​The admin panel and access key configuration are managed entirely on the client side for simplicity. The admin password is hardcoded in the index.html file. This is not a secure practice for a large-scale commercial application. It is a trade-off for creating a "serverless" application with these features. For a production environment with real paying customers, it is highly recommended to move the access key generation and validation logic to a secure backend server.