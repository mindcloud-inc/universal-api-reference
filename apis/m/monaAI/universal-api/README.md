# <img src="https://images.mindcloud.co/apps/icons/mona-ai_1776823511030.png" alt="Mona AI logo" width="28" height="28"> Mona AI: Universal API

Mona AI is an HR and staffing automation platform for recruiting workflows, matching, CV parsing, agents, webhooks, and pipeline automation.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/monaAI/latest
- **Category:** Human Resources / Recruiting
- **Actions:** 39
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.mona-ai.de/en
- **Vendor API docs:** https://api-docs.mona-ai.cloud/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check API Key Validity](actions/check-api-key-validity.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/check-api-key-validity?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (39)

### Agent

| Action | Method | Description |
| --- | --- | --- |
| [Get Agent Info](actions/get-agent-info.md) | GET | Retrieves a specific agent from Mona AI. |
| [Get Agents](actions/get-agents.md) | GET | Retrieves agents from Mona AI. |

### Agent Response

| Action | Method | Description |
| --- | --- | --- |
| [Get Agent Response](actions/get-agent-response.md) | GET | Gets a response from a Mona AI agent. |

### Agent Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Agent Result](actions/get-agent-result.md) | GET | Retrieves an agent result from Mona AI. |

### Agent Tool

| Action | Method | Description |
| --- | --- | --- |
| [Get Tools From Agent](actions/get-tools-from-agent.md) | GET | Retrieves tools for an agent from Mona AI. |

### Agent Workflow

| Action | Method | Description |
| --- | --- | --- |
| [Get Agent Workflow](actions/get-agent-workflow.md) | GET | Retrieves a workflow for a Mona AI agent. |

### Api Key Permission

| Action | Method | Description |
| --- | --- | --- |
| [Check API Key Permission](actions/check-api-key-permission.md) | GET | Checks whether a Mona AI API key has a specific permission. |

### Api Key Validity

| Action | Method | Description |
| --- | --- | --- |
| [Check API Key Validity](actions/check-api-key-validity.md) | GET | Checks whether a Mona AI API key is valid. |

### Applicant

| Action | Method | Description |
| --- | --- | --- |
| [Get Applicants](actions/get-applicants.md) | GET | Retrieves applicants from Mona AI. |

### Applicant Job Match

| Action | Method | Description |
| --- | --- | --- |
| [Match Applicant With Job Offer](actions/match-applicant-with-job-offer.md) | GET | Matches an applicant with a job offer in Mona AI. |

### Applicant Profile Sent

| Action | Method | Description |
| --- | --- | --- |
| [Get Profiles Sent By Applicant](actions/get-profiles-sent-by-applicant.md) | GET | Retrieves sent profiles for an applicant from Mona AI. |

### Company Knowledge

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Knowledge](actions/get-company-knowledge.md) | GET | Retrieves company knowledge from Mona AI. |

### Company Knowledge Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Company Knowledge](actions/search-company-knowledge.md) | GET | Finds company knowledge in Mona AI. |

### Document Text

| Action | Method | Description |
| --- | --- | --- |
| [Extract Document Text](actions/extract-document-text.md) | GET | Extracts text from a document in Mona AI. |

### Finished Applicant

| Action | Method | Description |
| --- | --- | --- |
| [Get Finished Applicants](actions/get-finished-applicants.md) | GET | Retrieves finished applicants from Mona AI. |

### Folder Content

| Action | Method | Description |
| --- | --- | --- |
| [Get Folder Contents](actions/get-folder-contents.md) | GET | Retrieves folder contents from Mona AI. |

### Interview

| Action | Method | Description |
| --- | --- | --- |
| [Get Interviews](actions/get-interviews.md) | GET | Retrieves interviews from Mona AI. |

### Job Offer

| Action | Method | Description |
| --- | --- | --- |
| [Get Job Offers](actions/get-job-offers.md) | GET | Retrieves job offers from Mona AI. |

### Job Offer Applicant Match

| Action | Method | Description |
| --- | --- | --- |
| [Match Job Offer With Applicants](actions/match-job-offer-with-applicants.md) | GET | Matches a job offer with applicants in Mona AI. |

### Knowledge Category

| Action | Method | Description |
| --- | --- | --- |
| [Get Knowledge Categories](actions/get-knowledge-categories.md) | GET | Retrieves knowledge categories from Mona AI. |

### Knowledge Structure

| Action | Method | Description |
| --- | --- | --- |
| [Get Knowledge Structure](actions/get-knowledge-structure.md) | GET | Retrieves the knowledge structure from Mona AI. |

### Matching Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Matching Results](actions/get-matching-results.md) | GET | Retrieves applicant matching results from Mona AI. |

### Mcp Health

| Action | Method | Description |
| --- | --- | --- |
| [MCP Health Check](actions/mcp-health-check.md) | GET | Retrieves MCP server health from Mona AI. |

### Mcp Tool

| Action | Method | Description |
| --- | --- | --- |
| [List MCP Tools](actions/list-mcp-tools.md) | GET | Retrieves MCP tools from Mona AI. |

### Monari Agent Response

| Action | Method | Description |
| --- | --- | --- |
| [Get Monari Agent Response](actions/get-monari-agent-response.md) | GET | Gets a response from a Mona AI Monari agent. |

### Parsed Applicant Cv

| Action | Method | Description |
| --- | --- | --- |
| [Parse Applicant CV](actions/parse-applicant-cv.md) | GET | Parses an applicant CV in Mona AI. |

### Parsed Cv

| Action | Method | Description |
| --- | --- | --- |
| [Parse CV Document](actions/parse-cv-document.md) | GET | Parses a CV document in Mona AI. |

### Pipeline

| Action | Method | Description |
| --- | --- | --- |
| [Get Pipeline](actions/get-pipeline.md) | GET | Retrieves a pipeline from Mona AI. |
| [List Pipelines](actions/list-pipelines.md) | GET | Retrieves pipelines from Mona AI. |

### Pipeline Execution

| Action | Method | Description |
| --- | --- | --- |
| [List Pipeline Executions](actions/list-pipeline-executions.md) | GET | Retrieves pipeline executions from Mona AI. |

### Profile Sent

| Action | Method | Description |
| --- | --- | --- |
| [Get Profiles Sent](actions/get-profiles-sent.md) | GET | Retrieves sent profiles from Mona AI. |

### Scheduled Workflow

| Action | Method | Description |
| --- | --- | --- |
| [Get Scheduled Workflows](actions/get-scheduled-workflows.md) | GET | Retrieves scheduled workflows from Mona AI. |

### Tool

| Action | Method | Description |
| --- | --- | --- |
| [Get All Tools](actions/get-all-tools.md) | GET | Retrieves all tools from Mona AI. |

### User Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get User Profile](actions/get-user-profile.md) | GET | Retrieves a user profile from Mona AI. |

### Workflow

| Action | Method | Description |
| --- | --- | --- |
| [Get Active Workflows](actions/get-active-workflows.md) | GET | Retrieves active workflows from Mona AI. |
| [Get Workflow](actions/get-workflow.md) | GET | Retrieves a workflow from Mona AI. |
| [List Workflows](actions/list-workflows.md) | GET | Retrieves workflows from Mona AI. |

### Workflow Execution

| Action | Method | Description |
| --- | --- | --- |
| [Get Workflow Execution](actions/get-workflow-execution.md) | GET | Retrieves a workflow execution from Mona AI. |
| [List Workflow Executions](actions/list-workflow-executions.md) | GET | Retrieves workflow executions from Mona AI. |

