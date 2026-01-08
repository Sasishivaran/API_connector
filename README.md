## Core Activity Steps (6 minutes):

- **Store the API Key Securely:**
  - Navigate to the "Plugins" tab in your Bubble editor, go to the "API" section, and add a new private key. Name it AI_Idea_Generator_Key and paste the key from the documentation.

<p align="center">
  <img src="https://github.com/Sasishivaran/API_images/blob/main/AI_IDEA.png" width="900">
</p>

- **Configure the API Connector:**
  - Go to the "Plugins" tab and open the API Connector. Create a new API call named  Get Idea. Configure the call with the correct Method (POST) and URL from the mock service documentation.

<p align="center">
  <img src="https://github.com/Sasishivaran/API_images/blob/main/Get_ID.png" width="900">
</p>

- **Add Authentication:**
  - Add the required Content-Type and Authorization headers. For the Authorization header, use the Bearer prefix followed by the dynamic private key you just saved in the secrets manager.

**Bubble API Connector Setup: (make sure to paste this to your API call setup)**

**API Call Name:** Get Idea  
**Method:** POST  
**API URL:** https://api.openai.com/v1/responses

**Headers:**  
**Key:** Content-Type     **Value:** application/json  
**Key:** Authorization     **Value:** Bearer sk*********

**Body Type:** JSON (Paste this exactly):
```json
{
  "model": "<model>",
  "input": "<prompt>",
  "stream": true
}
```
<p align="center">
  <img src="https://github.com/Sasishivaran/API_images/blob/main/key_Model.png" width="900">
</p>

**Key:** model  **Value:** gpt-5-nano  
**Key:** prompt  **Value:** “Tell me a joke”

- **Run a Test Call:**
  -  Add the simple JSON body provided in the mock service documentation and click "Initialize call.".
<p align="center">
  <img src="https://github.com/Sasishivaran/API_images/blob/main/Final.png" width="900">
</p>




