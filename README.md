# MinLink - URL Shortener  

MinLink is a simple and efficient URL shortener that converts long URLs into short, easy-to-share links. The application also generates QR codes for the shortened URLs.  

## Features  
✅ Shorten long URLs into compact links  
✅ Generate QR codes for each shortened link  
✅ Simple and elegant user interface  
✅ Copy shortened links with one click  
✅ Download QR codes for easy sharing  

## Tech Stack  
- **Frontend:** HTML, CSS, JavaScript  
- **Backend:** Node.js, Express.js    
- **Other:** QR Code generation using `qrcode` package  

## Installation  

1. **Clone the repository**  
   ```bash
   git clone https://github.com/your-repo/minlink-url-shortener.git
   cd minlink-url-shortener
   ```

2. **Install dependencies**  
   ```bash
   npm install
   ```

3. **Set up environment variables**  
   Create a `.env` file in the root directory and add the following:  
   ```ini
   BASE_URL=http://localhost:3000
   PORT=3000
   ```

4. **Run the server**  
   ```bash
   node server.js
   ```
   The server will start on `http://localhost:3000`.  

## API Endpoints  

### Shorten URL  
**POST** `/shorten`  
- **Body:** `{ "url": "https://abc.com" }`  
- **Response:** `{ "shortURL": "http://localhost:3000/abc123", "qrCodePath": "/qr/abc123.png" }`  

### Redirect to Original URL  
**GET** `/:shortId`  
- Redirects to the original URL associated with `shortId`  

## License  
This project is open-source and available under the [MIT License](LICENSE).  
