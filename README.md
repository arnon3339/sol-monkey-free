# SOL-MONKEY-FREE

This project is a full-stack application designed to showcase NFTs, with a frontend built using Next.js and two separate backends developed with FastAPI to handle NFT data and metadata. The platform integrates with the Solana blockchain to display minted NFTs and provides detailed information about each token.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)

## Overview

The NFT Showcase Platform allows users to browse and view NFTs minted on the Solana blockchain. The project is organized into three main directories:

- **frontend/**: Contains the Next.js application that serves as the user interface for showcasing NFTs.
- **backend/**: Contains the FastAPI backend service that provides APIs to the frontend for fetching NFT data images and properties. The main entry point for this backend is `index.py`.
- **metaread/**: A standalone FastAPI backend that reads minted NFTs from the Solana blockchain.

## Features

- **Showcase NFTs**: Display NFTs in an elegant and user-friendly interface.
- **Blockchain Integration**: Interact directly with the Solana blockchain to fetch and display real-time NFT data.
- **Detailed Metadata**: View comprehensive information about each NFT, including images and properties.

## Tech Stack

- **Frontend**: Next.js
- **Backends**: 
  - **Metaread Backend**: A FastAPI service that reads and processes data from the Solana blockchain.
  - **API Backend**: A FastAPI service that provides RESTful APIs for the frontend to fetch NFT data and properties. (Main entry point: `index.py`)
- **Blockchain**: Solana

## Installation

### Prerequisites

- Node.js (version 18.18.0)
- npm or yarn
- Python (version 3.10.0)
- FastAPI and Uvicorn
- Solana CLI (for blockchain interaction)

### Clone the Repository

```bash
git clone https://github.com/arnon3339/sol-monkey-free.git
cd sol-monkey-free
```

### Initialize the submodule 
If you haven't already initialized the submodule after cloning:

```bash
git submodule update --init --recursive
```

### Install Dependencies

For the frontend:

```bash
cd frontend
npm install
```

For the metaread backend:

```bash
cd metaread
pip install -r requirements.txt
```

For the API backend:

```bash
cd backend
pip install -r requirements.txt
```

### Environment Variables

Set up your environment variables for both backends in a `.env` file. for both frontend and backends.

### Running the Application

Start the frontend:

```bash
cd frontend
npm run dev
```

Start the metaread backend:

```bash
cd metaread
uvicorn index:app --reload
```

Start the API backend:

```bash
cd backend
uvicorn index:app --reload
```

## Usage

Once the application is running, navigate to `http://localhost:3000` in your browser to view the NFT showcase. You can interact with NFTs, view their images, and explore their properties.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
