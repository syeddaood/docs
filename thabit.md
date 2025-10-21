# 🚀 valleyair chat agent - User Guide

## 🌐 Access Your API Generator

**Live Application**: [https://thabit.up.railway.app](https://thabit.up.railway.app)

Visit the link above to access your LLM Parade application with the built-in API Generator functionality.

---

## 🔑 How to Generate Your API Key

### Step 1: Navigate to API Generator
1. **Open the Application**: Go to [https://thabit.up.railway.app](https://thabit.up.railway.app)
2. **Find the Sidebar**: Look for the navigation sidebar on the left side of the screen
3. **Click "API Generator"**: You'll see an option with a key icon (🔑) labeled "API Generator"

### Step 2: Generate Your Key
1. **Click "Generate New Key"**: This will create a new API key for our Valley Air District AI Agent
2. **Wait for Generation**: The process takes just a few seconds
3. **Copy Your Key**: Click the copy button (📋) to copy the key to your clipboard
4. **Store Securely**: Save your API key in a secure location

### Step 3: Verify Your Key
- Your generated key will start with `sk-` followed by 48 random characters
- Example format: `sk-abc123def456ghi789jkl012mno345pqr678stu901vwx234yz`
- The system will show a green checkmark when the key is valid

---

## 💬 How to Use Your API Key

### Method 1: Web Interface (Recommended)
The application automatically detects and uses your generated API key for chat sessions:

1. **Start Chatting**: Go to the "Chat" section in the sidebar
2. **Begin Conversation**: Your API key will be automatically used
3. **No Manual Entry Required**: The system handles authentication behind the scenes

### Method 2: Direct API Usage
Use your API key to interact with our Valley Air District AI Agent directly:

#### **API Endpoints Available:**

**Base URL**: `https://thabit.up.railway.app`

1. **Health Check**: `GET /api/status`
2. **Chat with AI**: `POST /api/chat`

#### **Step-by-Step API Usage:**

**Step 1: Check API Status**
```bash
curl https://thabit.up.railway.app/api/status
```

**Response:**
```json
{
  "status": "ok",
  "name": "llm-parade",
  "timestamp": "2024-12-19T10:30:00.000Z"
}
```

**Step 2: Chat with the AI Agent**
```bash
curl -X POST https://thabit.up.railway.app/api/chat \
  -H "Content-Type: application/json" \
  -d '{
    "messages": [
      {
        "isUser": true,
        "content": "What are the air quality regulations in the San Joaquin Valley?"
      }
    ],
    "model": "gpt-3.5-turbo",
    "apiKey": "sk-your-generated-api-key-here"
  }'
```

**Response:** Streaming text response from the Valley Air District AI Agent

#### **JavaScript Example:**
```javascript
const response = await fetch('https://thabit.up.railway.app/api/chat', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json',
  },
  body: JSON.stringify({
    messages: [
      {
        isUser: true,
        content: "Tell me about wildfire prevention programs"
      }
    ],
    model: 'gpt-3.5-turbo',
    apiKey: 'sk-your-generated-api-key-here'
  })
});

// Handle streaming response
const reader = response.body.getReader();
const decoder = new TextDecoder();

while (true) {
  const { done, value } = await reader.read();
  if (done) break;
  
  const chunk = decoder.decode(value);
  console.log(chunk); // This will stream the AI response
}
```

#### **Python Example:**
```python
import requests
import json

url = "https://thabit.up.railway.app/api/chat"
headers = {"Content-Type": "application/json"}
data = {
    "messages": [
        {
            "isUser": True,
            "content": "What permits do I need for my business?"
        }
    ],
    "model": "gpt-3.5-turbo",
    "apiKey": "sk-your-generated-api-key-here"
}

response = requests.post(url, headers=headers, json=data, stream=True)

for chunk in response.iter_content(chunk_size=1024):
    if chunk:
        print(chunk.decode('utf-8'), end='')
```

---

## 🏛️ Valley Air District AI Agent

### **Specialized Assistant**
Our API provides a specialized AI agent focused on the San Joaquin Valley Air District:

- **Air Quality Information**: Regulations, monitoring, and alerts
- **Permit Assistance**: Business permits and compliance requirements
- **Program Information**: Wildfire prevention, vehicle replacement, wood burning restrictions
- **Grants & Incentives**: Clean air initiatives and funding opportunities
- **Public Participation**: Board meetings and community engagement
- **Environmental Compliance**: Regulations and enforcement information

### **API Request Format**
```json
{
  "messages": [
    {
      "isUser": true,
      "content": "Your question about Valley Air District"
    }
  ],
  "model": "gpt-3.5-turbo",
  "apiKey": "sk-your-generated-api-key-here"
}
```

### **API Response Format**
- **Content-Type**: `text/plain`
- **Transfer-Encoding**: `chunked` (streaming)
- **Response**: Real-time streaming text from the AI agent

### **Example Questions You Can Ask:**
- "What are the current air quality regulations?"
- "How do I apply for a business permit?"
- "What wildfire prevention programs are available?"
- "Tell me about vehicle replacement incentives"
- "What are the wood burning restrictions?"
- "How can I participate in board meetings?"

---

## 🤖 Our AI Agent Capabilities

### **Valley Air District Specialization**
Our AI Agent is specifically designed to assist with San Joaquin Valley Air District services:

- **Air Quality Information**: Current regulations, monitoring data, and alerts
- **Permit Assistance**: Business permits, compliance requirements, and applications
- **Program Information**: Wildfire prevention, vehicle replacement, wood burning restrictions
- **Grants & Incentives**: Clean air initiatives and funding opportunities
- **Public Participation**: Board meetings, committees, and community engagement
- **Environmental Compliance**: Regulations, enforcement, and compliance guidance

### **Model Selection:**
1. **Go to "AI Models"**: Click on the AI Models section in the sidebar
2. **Browse Available Models**: See all supported models for our agent
3. **Select Your Preferred Model**: Choose based on your needs
4. **Start Chatting**: Your selected model will be used for conversations

---

## 🔧 Features Available

### ✅ What You Can Do:
- **Generate API Keys**: Create unlimited API keys for our Valley Air District AI Agent
- **Chat with AI**: Have conversations with our specialized Valley Air District assistant
- **Air Quality Information**: Get current regulations, monitoring data, and alerts
- **Permit Assistance**: Get help with business permits and compliance requirements
- **Program Information**: Learn about wildfire prevention, vehicle replacement, and wood burning programs
- **Grant Information**: Discover clean air initiatives and funding opportunities
- **Public Participation**: Learn about board meetings and community engagement

### 🎯 Use Cases:
- **Business Compliance**: Get help with air quality permits and regulations
- **Community Information**: Learn about Valley Air District programs and services
- **Environmental Education**: Understand air quality regulations and compliance
- **Program Discovery**: Find grants, incentives, and assistance programs
- **Public Engagement**: Learn about board meetings and public participation opportunities
- **Research**: Gather information about Valley Air District policies and procedures

---

## 🛡️ Security & Best Practices

### 🔒 Keep Your Keys Secure:
- **Never Share Publicly**: Don't post API keys on social media or forums
- **Use HTTPS Only**: Always access the app via secure connection
- **Regenerate When Needed**: Create new keys if compromised
- **Monitor Usage**: Keep track of your API usage

### 💡 Tips for Better Experience:
- **Clear Prompts**: Write specific, detailed prompts for better responses
- **Use Context**: Provide background information for complex Valley Air District questions
- **Iterate**: Refine your prompts based on initial responses
- **Save Important Keys**: Keep copies of working API keys

---

## 🚨 Important Limitations

### Current Restrictions:
- **Valley Air District Focus Only**: Our AI agent specializes only in San Joaquin Valley Air District topics
- **No General AI**: Cannot answer questions unrelated to air quality, permits, or district services
- **Session Storage**: API keys are stored only for the current browser session
- **Streaming Responses**: All responses are streamed in real-time

### Future Expansions:
- **Enhanced Key Management**: Persistent key storage and management
- **Team Features**: Shared keys and collaborative features
- **Advanced Analytics**: Usage statistics and reporting
- **Integration APIs**: Programmatic key management

---

## 🔍 Troubleshooting

### Common Issues:

#### **"Failed to Generate API Key"**
- **Solution**: Refresh the page and try again
- **Cause**: Temporary browser or network issues

#### **"Copy Failed"**
- **Solution**: Manually select and copy the key text
- **Cause**: Browser clipboard permissions

#### **"Invalid API Key"**
- **Solution**: Generate a new key
- **Cause**: Corrupted or manually edited key

#### **"Model Not Available"**
- **Solution**: Try a different OpenAI model
- **Cause**: Model temporarily unavailable or not supported

#### **API Error Responses:**

**400 Bad Request - Missing API Key:**
```json
{
  "error": "API key is required. Please provide it in the request body."
}
```

**500 Internal Server Error - AI Agent Error:**
```json
{
  "error": "AI Agent error: [error details]"
}
```

**500 Internal Server Error - Stream Error:**
```json
{
  "error": "Stream error occurred"
}
```

#### **API Troubleshooting:**

1. **Check API Status First:**
   ```bash
   curl https://thabit.up.railway.app/api/status
   ```

2. **Verify API Key Format:**
   - Must start with `sk-`
   - Must be at least 20 characters long
   - No spaces or special characters

3. **Test with Simple Request:**
   ```bash
   curl -X POST https://thabit.up.railway.app/api/chat \
     -H "Content-Type: application/json" \
     -d '{"messages":[{"isUser":true,"content":"Hello"}],"apiKey":"sk-your-key"}'
   ```

4. **Check Network Connectivity:**
   - Ensure you can reach `thabit.up.railway.app`
   - Check firewall settings
   - Verify HTTPS connection

### Getting Help:
- **Check Status**: Visit the app's status page for service updates
- **Refresh Browser**: Clear cache and reload the page
- **Try Different Browser**: Switch to Chrome, Firefox, or Safari
- **Contact Support**: Report persistent issues through the app

---

## 📊 Usage Monitoring

### Track Your Usage:
1. **Monitor API Calls**: Keep track of your API usage through our system
2. **Check Response Quality**: Review the quality of Valley Air District responses
3. **Optimize Prompts**: Use efficient prompts for better results
4. **Monitor Activity**: Review your API key usage patterns

### Best Practices:
- **Focused Questions**: Ask specific questions about Valley Air District topics
- **Clear Context**: Provide relevant background for complex queries
- **Efficient Prompts**: Use clear, specific language for better responses
- **Appropriate Topics**: Stick to air quality, permits, and district services

---

## 🎉 Getting Started Checklist

- [ ] **Visit**: Go to [https://thabit.up.railway.app](https://thabit.up.railway.app)
- [ ] **Navigate**: Click "API Generator" in the sidebar
- [ ] **Generate**: Create your first API key
- [ ] **Copy**: Save your key securely
- [ ] **Test**: Try chatting with an AI model
- [ ] **Explore**: Check out different features and models
- [ ] **Monitor**: Set up usage tracking in OpenAI dashboard

---

## 📞 Support & Resources

### Helpful Links:
- **Live App**: [https://thabit.up.railway.app](https://thabit.up.railway.app)
- **Valley Air District**: [valleyair.org](https://valleyair.org)
- **API Documentation**: This guide contains all API information
- **Status Check**: [https://thabit.up.railway.app/api/status](https://thabit.up.railway.app/api/status)

### Need More Help?
- **Check Documentation**: Review this guide for common solutions
- **Browser Issues**: Try refreshing or using a different browser
- **Network Problems**: Check your internet connection
- **Service Status**: Verify the app is running properly

---

**🎯 Ready to Start?** Visit [https://thabit.up.railway.app](https://thabit.up.railway.app) and click "API Generator" to create your first API key!

---

*Last Updated: December 2024*  
*Version: 1.0*  
*Specialized for: San Joaquin Valley Air District Services*
