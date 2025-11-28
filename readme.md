# API Testing Client

A modern, user-friendly web-based API testing tool built with pure HTML, CSS, and JavaScript. Test RESTful APIs with an intuitive interface featuring syntax highlighting, request history, and comprehensive response analysis. The main purpose for this is to support learning API backend programs and testing personal project API endpoints.

## Features

### Core Functionality
- **Multiple HTTP Methods**: Support for GET, POST, PUT, and DELETE requests
- **Custom Headers**: Add unlimited custom headers to your requests
- **Query Parameters**: Easily add and manage URL query parameters
- **Request Body**: JSON body support for POST and PUT requests with validation
- **Timeout Configuration**: Set custom timeout values for your requests

### Response Analysis
- **Tabbed Response View**: Switch between Body, Headers, and Raw views
- **Syntax Highlighting**: JSON responses are beautifully formatted with color-coded syntax
- **Status Indicators**: Clear visual feedback for successful and failed requests
- **Response Time**: Track how long each request takes
- **Copy to Clipboard**: One-click copying of response data

### User Experience
- **Request History**: Automatically saves the last 10 requests with timestamp
- **Quick Reload**: Click any history item to reload that request
- **Loading States**: Visual feedback while requests are in progress
- **Error Handling**: Clear error messages for network failures and timeouts
- **Responsive Design**: Works on desktop and mobile devices

## Getting Started

### Installation

No installation required! Simply download the HTML file and open it in any modern web browser.

```bash
# Download the file
# Then open it in your browser
open api-tester.html
```

Or double-click the file to open it in your default browser.

### Basic Usage

1. **Select HTTP Method**: Click one of the method buttons (GET, POST, PUT, DELETE)
2. **Enter URL**: Type or paste your API endpoint URL
3. **Add Query Parameters** (Optional):
   - Click "Add Parameter"
   - Enter key and value pairs
   - Remove unwanted parameters with the trash icon

4. **Add Headers** (Optional):
   - Click "Add Header"
   - Common headers: `Content-Type`, `Authorization`, `Accept`
   - Example: `Authorization: Bearer your-token-here`

5. **Add Request Body** (POST/PUT only):
   - Enter valid JSON in the request body textarea
   - Example: `{"name": "John", "email": "john@example.com"}`

6. **Configure Timeout** (Optional):
   - Set request timeout in milliseconds (default: 30000ms / 30 seconds)

7. **Send Request**: Click the "Send Request" button

8. **View Response**:
   - Check the status code and response time
   - Switch between Body, Headers, and Raw tabs
   - Copy response data using the Copy button

## Examples

### GET Request
```
Method: GET
URL: https://jsonplaceholder.typicode.com/users/1
Headers: (none required)
```

### POST Request with JSON Body
```
Method: POST
URL: https://jsonplaceholder.typicode.com/posts
Headers:
  Content-Type: application/json
Body:
{
  "title": "My Post",
  "body": "This is the post content",
  "userId": 1
}
```

### Authenticated Request
```
Method: GET
URL: https://api.example.com/user/profile
Headers:
  Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...
  Content-Type: application/json
```

### Request with Query Parameters
```
Method: GET
URL: https://api.example.com/search
Parameters:
  q: javascript
  limit: 10
  sort: date
```

## Features in Detail

### Request Configuration

**HTTP Methods**
- **GET**: Retrieve data from the server
- **POST**: Send new data to the server
- **PUT**: Update existing data on the server
- **DELETE**: Remove data from the server

**Headers**
Custom headers allow you to:
- Set content types (`Content-Type: application/json`)
- Add authentication (`Authorization: Bearer token`)
- Specify accepted response formats (`Accept: application/json`)
- Add custom headers for your API requirements

**Query Parameters**
Query parameters are automatically encoded and appended to the URL. They're perfect for:
- Search queries
- Filtering results
- Pagination
- Sorting options

### Response Display

**Body Tab**
- Shows the response data with syntax highlighting
- JSON responses are automatically formatted and color-coded
- Text responses are displayed as-is

**Headers Tab**
- Displays all response headers
- Useful for debugging CORS issues, checking cache headers, etc.

**Raw Tab**
- Shows the unformatted response data
- Useful for copying raw JSON or text

### Request History

The last 10 requests are automatically saved with:
- HTTP method used
- Full URL with parameters
- Response status code
- Response time
- Timestamp

Click any history item to reload that request's response.

## Browser Compatibility

This tool works in all modern browsers:
- Chrome/Edge (v90+)
- Firefox (v88+)
- Safari (v14+)
- Opera (v76+)

### Required Browser Features
- `fetch()` API
- ES6+ JavaScript
- CSS Grid
- Async/await

## Security Considerations

### CORS (Cross-Origin Resource Sharing)
This tool runs in your browser, so it's subject to CORS restrictions. If you get CORS errors:
- The API must include proper CORS headers
- Use a CORS proxy for testing (not recommended for production)
- Test APIs that allow cross-origin requests

### Sensitive Data
- Be cautious when entering API keys or tokens
- This tool doesn't store data persistently, but avoid using it on shared computers
- Clear your browser history if you've entered sensitive information

## Limitations

- **CORS**: Cannot bypass browser CORS restrictions
- **Authentication**: No built-in OAuth flow support
- **File Uploads**: Does not support multipart/form-data or file uploads
- **WebSocket**: Only supports HTTP/HTTPS requests, not WebSocket connections
- **Request Body**: Only supports JSON for POST/PUT requests

## Troubleshooting

**"Request failed: NetworkError"**
- Check your internet connection
- Verify the URL is correct and accessible
- Check if the API requires authentication

**CORS Error**
- The API server must include appropriate CORS headers
- Try using a CORS-enabled API or CORS proxy for testing

**"Invalid JSON in request body"**
- Ensure your JSON is properly formatted
- Use a JSON validator to check syntax
- Common issues: trailing commas, unquoted keys

**Request Timeout**
- Increase the timeout value if the API is slow
- Check your network connection
- Verify the API endpoint is responding

## Tips and Best Practices

1. **Save Your Requests**: Use the history feature to save frequently used requests
2. **Test Error Cases**: Try invalid data to see how APIs handle errors
3. **Check Response Headers**: They often contain useful debugging information
4. **Start Simple**: Test with GET requests before moving to POST/PUT
5. **Use Public APIs**: Try jsonplaceholder.typicode.com for safe testing

## Public APIs for Testing

Here are some free, public APIs you can use to test this tool:

- **JSONPlaceholder**: https://jsonplaceholder.typicode.com/posts
- **REQ|RES**: https://reqres.in/api/users
- **Cat Facts**: https://catfact.ninja/fact
- **Open Notify (ISS Location)**: http://api.open-notify.org/iss-now.json
- **Random User**: https://randomuser.me/api/

## Technical Details

**Built With**
- Pure vanilla JavaScript (no frameworks)
- CSS3 with Grid and Flexbox
- HTML5 Fetch API
- No external dependencies

**File Size**
- Single HTML file (~25KB)
- No external CSS or JS files needed
- Works completely offline once loaded

## License

This project is free to use, modify, and distribute.

## Contributing

Feel free to modify and enhance this tool for your needs. Some ideas for improvements:
- Add support for file uploads
- Include request/response snippets in different languages
- Add environment variables for API endpoints
- Implement request collections or saved presets
- Add GraphQL support

## Support

For issues or questions:
- Check the Troubleshooting section above
- Verify your browser supports all required features
- Test with a known-working API endpoint first

---

**Happy API Testing! 🚀**
