# Here’s a concise cURL cheat sheet covering essential commands and options

---

### **Basic Commands**

- **GET Request**
  ```bash
  curl https://example.com
  ```
- **POST Request**
  ```bash
  curl -X POST https://example.com
  ```
- **PUT Request**
  ```bash
  curl -X PUT https://example.com
  ```
- **DELETE Request**
  ```bash
  curl -X DELETE https://example.com
  ```

---

### **Headers**

- **Add a Header**
  ```bash
  curl -H "Content-Type: application/json" https://example.com
  ```
- **Multiple Headers**
  ```bash
  curl -H "Authorization: Bearer token" -H "Accept: application/json" https://example.com
  ```

---

### **Data & Payload**

- **Send JSON Data (POST/PUT)**
  ```bash
  curl -X POST -H "Content-Type: application/json" -d '{"key1":"value1", "key2":"value2"}' https://example.com
  ```
- **Send Form Data**
  ```bash
  curl -X POST -F "name=John" -F "age=30" https://example.com
  ```

---

### **Authentication**

- **Basic Authentication**
  ```bash
  curl -u username:password https://example.com
  ```
- **Bearer Token**
  ```bash
  curl -H "Authorization: Bearer token" https://example.com
  ```

---

### **File Uploads & Downloads**

- **Upload a File**
  ```bash
  curl -X POST -F "file=@/path/to/file" https://example.com/upload
  ```
- **Download a File**
  ```bash
  curl -O https://example.com/file.zip
  ```

---

### **Handling Responses**

- **Save Response to File**
  ```bash
  curl -o output.txt https://example.com
  ```
- **Follow Redirects**
  ```bash
  curl -L https://example.com
  ```
- **Verbose Output**
  ```bash
  curl -v https://example.com
  ```

---

### **Security**

- **Ignore SSL Certificate Errors**
  ```bash
  curl -k https://example.com
  ```
- **Specify SSL/TLS Version**
  ```bash
  curl --tlsv1.2 https://example.com
  ```

---

### **Miscellaneous**

- **Custom User-Agent**
  ```bash
  curl -A "Mozilla/5.0" https://example.com
  ```
- **Limit Request Speed**
  ```bash
  curl --limit-rate 100k https://example.com
  ```
- **Send Cookies**
  ```bash
  curl -b "name=value" https://example.com
  ```

---

### **Examples**

- **GET with Custom Header and Query Parameters**
  ```bash
  curl -G -H "Accept: application/json" -d "key=value" https://example.com
  ```
- **POST with Bearer Token and JSON Payload**
  ```bash
  curl -X POST -H "Authorization: Bearer token" -H "Content-Type: application/json" -d '{"key":"value"}' https://example.com
  ```
- **Upload File and Form Data**
  ```bash
  curl -X POST -F "name=John" -F "file=@/path/to/file" https://example.com/upload
  ```

---

This cheat sheet should help you quickly recall the most common cURL commands and options.
