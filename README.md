# AI GitHub Repository Analyzer

## Overview
The AI GitHub Repository Analyzer is an automation workflow built using **n8n**. It accepts a GitHub repository URL through a webhook, extracts the repository owner and name, fetches repository details using the GitHub REST API, and returns important information in JSON format.

## Features
- Accepts GitHub repository URL via Webhook
- Extracts repository owner and repository name
- Retrieves repository details using GitHub API
- Returns formatted JSON response
- No authentication required for public repositories
- Built using n8n low-code automation platform

## Workflow

Webhook
↓
Code (JavaScript)
↓
HTTP Request (GitHub API)
↓
Edit Fields
↓
Respond to Webhook

## Technologies Used
- n8n
- JavaScript
- GitHub REST API
- Webhooks
- Hoppscotch (API Testing)

## Input Example

```json
{
  "url": "https://github.com/n8n-io/n8n"
}
```

## Output Example

```json
{
  "Repository": "n8n",
  "Description": "Fair-code workflow automation platform with native AI capabilities.",
  "Stars": "195935",
  "Forks": "59222",
  "Open Issues": "1456",
  "Default Branch": "master"
}
```

## Project Structure

```
n8n-project/
│
├── README.md
├── workflow.json
├── AI_GitHub_Repository_Analyzer_Report.pdf
├── AI_GitHub_Repository_Analyzer_PPT.pptx
└── screenshots/
```

## How to Run

1. Import the workflow into n8n.
2. Configure the Webhook node.
3. Execute the workflow.
4. Send a POST request using Hoppscotch or Postman.
5. Provide a GitHub repository URL in JSON format.
6. Receive repository details as the response.

## Example Request

POST

```
https://your-n8n-instance/webhook/github-analyzer
```

Body

```json
{
  "url": "https://github.com/n8n-io/n8n"
}
```

## Author

**Vidhi Kore**

Second Year B.Tech (CSE - Data Science & Emerging Technology)

S.B. Jain Institute of Technology, Management & Research, Nagpur
