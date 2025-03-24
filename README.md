# Chunks Creator

**Chunks Creator** is a web-based application built with **Node.js**, **Next.js**, **React**, and **Redux** for creating, managing, and visualizing chunks of data that can be used in embedding systems. The system leverages **Mistral technologies** for advanced data processing and embedding compatibility.

---

## Features

- **Chunk Creation**: Easily create chunks with customizable fields (e.g., title, content, metadata).
- **Chunk Management**: Edit, delete, and organize chunks efficiently.
- **Visualization**: Interactive dashboard to view and explore chunks.
- **Embedding Integration**: Export chunks in formats compatible with embedding systems.
- **Mistral Integration**: Utilize Mistral technologies for advanced data processing and embedding optimization.
- **Responsive Design**: Works seamlessly on desktop, tablet, and mobile devices.

---

## Tech Stack

- **Frontend**: Next.js, React, Redux, Tailwind CSS
- **Backend**: Node.js, Express.js
- **Database**: MongoDB/PostgreSQL
- **AI/ML**: Mistral technologies
- **Deployment**: Vercel, Docker

---

## Getting Started

### Prerequisites

- Node.js (v18 or higher)
- npm or yarn
- MongoDB/PostgreSQL database
- Mistral API key (if required)

### Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/NikolayGechev/chunks_creator.git
   cd chunks-creator
   ```

2. **Install dependencies**:
   ```bash
   npm install
   # or
   yarn install
   ```

3. **Set up environment variables**:
   Create a `.env` file in the root directory and add the following variables:
   ```env
   DATABASE_URL=mongodb://localhost:27017/chunksdb
   MISTRAL_API_KEY=your_mistral_api_key
   NEXT_PUBLIC_API_URL=http://localhost:3000/api
   ```

4. **Run the development server**:
   ```bash
   npm run dev
   # or
   yarn dev
   ```

5. **Open the application**:
   Visit `http://localhost:3000` in your browser.

---

## Project Structure

```
chunks-creator/
├── client/               # Frontend (Next.js, React, Redux)
│   ├── components/       # Reusable React components
│   ├── pages/            # Next.js pages
│   ├── store/            # Redux store and slices
│   └── styles/           # CSS or Tailwind styles
├── server/               # Backend (Node.js, Express.js)
│   ├── controllers/      # API controllers
│   ├── models/           # Database models
│   ├── routes/           # API routes
│   └── utils/            # Utility functions
├── .env                  # Environment variables
├── .gitignore            # Git ignore file
├── package.json          # Node.js dependencies
└── README.md             # Project documentation
```

---

## Using Mistral Technologies

The system integrates **Mistral technologies** for advanced data processing and embedding optimization. Here's how it works:

1. **Chunk Processing**:
   - When a chunk is created, it is sent to the Mistral API for processing (e.g., embedding generation, metadata extraction).
   - The processed data is stored in the database and displayed in the UI.

2. **Embedding Export**:
   - Chunks can be exported in formats optimized for embedding systems using Mistral's output formats.

3. **API Integration**:
   - The backend communicates with the Mistral API using the provided API key.
   - Example API call:
     ```javascript
     const response = await fetch('https://api.mistral.ai/process', {
       method: 'POST',
       headers: {
         'Content-Type': 'application/json',
         'Authorization': `Bearer ${process.env.MISTRAL_API_KEY}`,
       },
       body: JSON.stringify({ chunk: chunkData }),
     });
     ```

---

## Deployment

### Vercel (Frontend)
1. Install Vercel CLI:
   ```bash
   npm install -g vercel
   ```
2. Deploy:
   ```bash
   vercel
   ```

### Docker (Backend)
1. Build the Docker image:
   ```bash
   docker build -t chunks-creator .
   ```
2. Run the container:
   ```bash
   docker run -p 3000:3000 chunks-creator
   ```

---

## Contributing

Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a pull request.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Acknowledgments

- **Mistral Technologies** for providing advanced data processing capabilities.
- **Next.js** and **React** for building a powerful frontend.
- **Node.js** for a robust backend.

---

For any questions or issues, please open an issue on GitHub or contact the project maintainers.

---

This README provides a comprehensive overview of your project and should help users and contributors get started quickly. Let me know if you need further customization!