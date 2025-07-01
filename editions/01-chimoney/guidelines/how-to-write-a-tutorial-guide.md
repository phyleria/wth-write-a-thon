# How to Write a Tutorial Guide

A tutorial guide shows someone how to use the API endpoint in a practical, step-by-step way. It should help the reader go from “I’ve never used this API” to “I just made my first successful API call.”

This guide walks you through how to structure your tutorial and make it useful for developers at any level.

## 1. Set a clear goal

Start by explaining what the tutorial will help the reader achieve. Be specific.

Example:
> In this tutorial, you’ll learn how to use Chimoney’s `payout-to-wallet` endpoint to send money to an Interledger wallet address.

## 2. List the requirements

Tell readers what they need to follow along:

- A Chimoney developer account
- API key or token
- Tool like Postman or curl
- (Optional) A code environment (e.g., Node.js, Python, etc.)

Use a bullet list like this:

```md
### Prerequisites
- Chimoney API key
- Wallet address to test
- Postman or curl installed
```

## 3. Break down the steps
Walk through the process clearly. Common structure:
1. Set up authentication
1. Prepare your request (method, URL, headers, body)
1. Send the request
1. Check the response
1. Handle errors (optional)
Use real sample data where possible — no placeholders like your-key-here.

## 4. Include sample code or commands
Make it easy to follow with concrete examples:
Sample cURL:
```
curl -X POST https://api.chimoney.io/payouts \
-H "Authorization: Bearer YOUR_API_KEY" \
-H "Content-Type: application/json" \
-d '{"wallet": "ilp-wallet-address", "amount": 50, "currency": "USD"}'
```
Sample Postman JSON:
Show what the request body looks like.

## 5. Explain what’s happening
After each code example, explain it in plain English:
- What does each parameter do?
- What should the response contain?
- What does success or failure look like?

Example:
> This call sends a $50 payout to the specified wallet. You’ll receive a 200 OK if successful, and a transaction ID in the response.

## 6. Add a recap or next step
At the end, summarize what the user accomplished and suggest what they can do next.

Example:
> Now that you’ve successfully made a payout, you can explore batch payments or add error handling to your integration.

## Tutorial checklist
- Clear goal at the beginning
- Setup and prerequisites explained
- Request/response examples included
- Each step explained in simple terms
- Error handling or common issues addressed
- Tutorial flows from start to finish logically

## Final tip
Write as if the reader is new to the API, but not new to coding. Keep it friendly, technical, and focused.
