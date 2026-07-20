# Mona AI: Native API Reference

A consolidated summary of Mona AI's API configuration and 39 documented operations, with links to official documentation.

- **Official docs:** https://api-docs.mona-ai.cloud/
- **API base URL:** `https://api.mona-ai.cloud`

## Authentication

### Mona API Key

Authenticate with Mona using a bearer API key plus the account uid companion field.

### Credentials

- **API Key:** `apiKey` · required · Mona API key used for the X-API-Key request header and JSON body.
- **UID:** `uid` · required · Mona account user identifier required in endpoint JSON bodies.

[Official authentication documentation](https://api-docs.mona-ai.cloud/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (39 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check API Key Permission](actions/check-api-key-permission.md) | `POST /auth/checkIfAPIKeyHasPermission` | [docs](https://api-docs.mona-ai.cloud/) |
| [Check API Key Validity](actions/check-api-key-validity.md) | `POST /auth/checkIfAPIKeyIsValid` | [docs](https://api-docs.mona-ai.cloud/) |
| [Extract Document Text](actions/extract-document-text.md) | `POST /parsing/AnyDocumentToText` | [docs](https://api-docs.mona-ai.cloud/) |
| [Get Active Workflows](actions/get-active-workflows.md) | `POST /agent/getActiveWorkflows` | [docs](https://api-docs.mona-ai.cloud/) |
| [Get Agent Info](actions/get-agent-info.md) | `POST /agent/getAgentInfo` | [docs](https://api-docs.mona-ai.cloud/) |
| [Get Agent Response](actions/get-agent-response.md) | `POST /agent/getAgentResponse` | [docs](https://api-docs.mona-ai.cloud/) |
| [Get Agent Result](actions/get-agent-result.md) | `POST /agent/getAgentResult` | [docs](https://api-docs.mona-ai.cloud/) |
| [Get Agent Workflow](actions/get-agent-workflow.md) | `POST /agent/getAgentWorkflow` | [docs](https://api-docs.mona-ai.cloud/) |
| [Get Agents](actions/get-agents.md) | `POST /database/getAgentsFromDatabase` | [docs](https://api-docs.mona-ai.cloud/) |
| [Get All Tools](actions/get-all-tools.md) | `POST /database/getAllTools` | [docs](https://api-docs.mona-ai.cloud/) |
| [Get Applicants](actions/get-applicants.md) | `POST /database/getApplicantsFromDatabase` | [docs](https://api-docs.mona-ai.cloud/) |
| [Get Company Knowledge](actions/get-company-knowledge.md) | `POST /companyKnowledge/getKnowledge` | [docs](https://api-docs.mona-ai.cloud/) |
| [Get Finished Applicants](actions/get-finished-applicants.md) | `POST /database/getFinishedApplicantsFromDatabase` | [docs](https://api-docs.mona-ai.cloud/) |
| [Get Folder Contents](actions/get-folder-contents.md) | `POST /companyKnowledge/getFolderContents` | [docs](https://api-docs.mona-ai.cloud/) |
| [Get Interviews](actions/get-interviews.md) | `POST /database/getInterviewsFromDatabase` | [docs](https://api-docs.mona-ai.cloud/) |
| [Get Job Offers](actions/get-job-offers.md) | `POST /database/getJobOffersFromDatabase` | [docs](https://api-docs.mona-ai.cloud/) |
| [Get Knowledge Categories](actions/get-knowledge-categories.md) | `POST /companyKnowledge/getCategories` | [docs](https://api-docs.mona-ai.cloud/) |
| [Get Knowledge Structure](actions/get-knowledge-structure.md) | `POST /companyKnowledge/getKnowledgeStructure` | [docs](https://api-docs.mona-ai.cloud/) |
| [Get Matching Results](actions/get-matching-results.md) | `POST /matching/getMatchingResults` | [docs](https://api-docs.mona-ai.cloud/) |
| [Get Monari Agent Response](actions/get-monari-agent-response.md) | `POST /agent/getMonariAgentResponse` | [docs](https://api-docs.mona-ai.cloud/) |
| [Get Pipeline](actions/get-pipeline.md) | `POST /pipeline/get` | [docs](https://api-docs.mona-ai.cloud/) |
| [Get Profiles Sent](actions/get-profiles-sent.md) | `POST /matching/getProfilesSent` | [docs](https://api-docs.mona-ai.cloud/) |
| [Get Profiles Sent By Applicant](actions/get-profiles-sent-by-applicant.md) | `POST /matching/getProfilesSentByApplicantId` | [docs](https://api-docs.mona-ai.cloud/) |
| [Get Scheduled Workflows](actions/get-scheduled-workflows.md) | `POST /agent/getScheduledWorkflows` | [docs](https://api-docs.mona-ai.cloud/) |
| [Get Tools From Agent](actions/get-tools-from-agent.md) | `POST /database/getToolsFromAgent` | [docs](https://api-docs.mona-ai.cloud/) |
| [Get User Profile](actions/get-user-profile.md) | `POST /agent/getUserProfile` | [docs](https://api-docs.mona-ai.cloud/) |
| [Get Workflow](actions/get-workflow.md) | `POST /agent/getWorkflow` | [docs](https://api-docs.mona-ai.cloud/) |
| [Get Workflow Execution](actions/get-workflow-execution.md) | `POST /agent/getWorkflowExecution` | [docs](https://api-docs.mona-ai.cloud/) |
| [List MCP Tools](actions/list-mcp-tools.md) | `GET /mcp/tools` | [docs](https://api-docs.mona-ai.cloud/) |
| [List Pipeline Executions](actions/list-pipeline-executions.md) | `POST /pipeline/executions` | [docs](https://api-docs.mona-ai.cloud/) |
| [List Pipelines](actions/list-pipelines.md) | `POST /pipeline/list` | [docs](https://api-docs.mona-ai.cloud/) |
| [List Workflow Executions](actions/list-workflow-executions.md) | `POST /agent/listWorkflowExecutions` | [docs](https://api-docs.mona-ai.cloud/) |
| [List Workflows](actions/list-workflows.md) | `POST /agent/listWorkflows` | [docs](https://api-docs.mona-ai.cloud/) |
| [Match Applicant With Job Offer](actions/match-applicant-with-job-offer.md) | `POST /matching/applicantWithJobOffer` | [docs](https://api-docs.mona-ai.cloud/) |
| [Match Job Offer With Applicants](actions/match-job-offer-with-applicants.md) | `POST /matching/jobOfferWithMultipleApplicants` | [docs](https://api-docs.mona-ai.cloud/) |
| [MCP Health Check](actions/mcp-health-check.md) | `GET /mcp/health` | [docs](https://api-docs.mona-ai.cloud/) |
| [Parse Applicant CV](actions/parse-applicant-cv.md) | `POST /parsing/parseApplicantCV` | [docs](https://api-docs.mona-ai.cloud/) |
| [Parse CV Document](actions/parse-cv-document.md) | `POST /parsing/parseCV` | [docs](https://api-docs.mona-ai.cloud/) |
| [Search Company Knowledge](actions/search-company-knowledge.md) | `POST /companyKnowledge/searchKnowledge` | [docs](https://api-docs.mona-ai.cloud/) |
