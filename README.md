# Domain OSINT Automation

This project is an **n8n-powered automation workflow** that performs OSINT and reconnaissance on any domain name using public APIs and AI-based summarization.

## How It Works

### **1. User Interaction**

Users trigger the workflow by submitting a **domain name** (e.g., `example.com`) through Telegram.  
n8n then automatically begins scanning and collecting intelligence on the provided domain.

### **2. API-Based Domain Scanning**

The workflow uses public APIs to gather:

- Domain registration details (WHOIS)
    
- DNS records
    
- Subdomains
    
- Email configuration
    
- Hosting information
    
- SSL details
    
- Reputation and security flags
    

This provides a full snapshot of the domain’s identity, infrastructure, and attack surface.

### **3. AI Summarization**

Many APIs return large, highly detailed JSON responses.  
To convert this into usable intelligence:

- An **AI Summarization Node** in n8n extracts the essential details
    
- Converts raw API JSON → structured, clean JSON
    
- Generates readable summaries and analyst-style insights
    

### **4. Report Generation**

The workflow combines:

- API findings
    
- AI-generated summaries
    
- Infrastructure breakdown
    
- Subdomain analysis
    

into a final **Markdown OSINT Report** that is sent back to the user.

---

## Screenshots

- **User Input Example**  
    ![[src/input.png]]
    
- **Generated Output Example**  
    ![[src/output.png]]
