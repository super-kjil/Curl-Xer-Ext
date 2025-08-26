# MS Word Document Extractor

A Laravel + React application that extracts domain names from Microsoft Word (.docx) documents.

## Features

- **File Upload**: Drag and drop or click to upload .docx files
- **Domain Extraction**: Automatically extracts domain names from document content
- **Copy Functionality**: Copy extracted domains or full text to clipboard
- **Modern UI**: Built with Shadcn UI components and Tailwind CSS
- **Responsive Design**: Works on desktop and mobile devices

## How to Use

1. **Navigate to the Extractor**: Go to `/domain-extractor` in your application
2. **Upload a Document**: Drag and drop a .docx file or click to browse
3. **View Results**: The app will display:
   - Extracted domain names (cleaned and deduplicated)
   - Full text content from the document
4. **Copy Content**: Use the copy buttons to copy domains or full text to clipboard

## Domain Extraction

The app uses regex patterns to identify domain names in the document:
- Supports domains with or without `http://` or `https://` prefixes
- Automatically removes `www.` prefixes
- Deduplicates and sorts domains alphabetically
- Handles various domain formats (e.g., `example.com`, `sub.example.co.uk`)
- Handles varoius IPV4 (e.g., `192.168.0.1`)

## Technical Details

- **Frontend**: React + TypeScript + Tailwind CSS
- **UI Components**: Shadcn UI + Radix UI primitives
- **File Processing**: Mammoth.js for .docx parsing
- **File Upload**: React Dropzone for drag & drop functionality
- **Notifications**: Toast notifications for user feedback

## Installation

1. Clone the repository
2. Install PHP dependencies: `composer install`
3. Install Node.js dependencies: `npm install`
4. Set up your environment file: `cp .env.example .env`
5. Generate application key: `php artisan key:generate`
6. Run database migrations: `php artisan migrate`
7. Build frontend assets: `npm run build`
8. Start the development server: `php artisan serve`

## Development

- **Frontend Development**: `npm run dev`
- **Build for Production**: `npm run build`
- **Type Checking**: `npm run types`
- **Linting**: `npm run lint`

## Requirements

- PHP 8.1+
- Node.js 18+
- Laravel 11+
- Modern web browser with clipboard API support

## Browser Support

The app requires modern browser features:
- File API for file uploads
- Clipboard API for copy functionality
- ES6+ JavaScript support

## License

This project is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
