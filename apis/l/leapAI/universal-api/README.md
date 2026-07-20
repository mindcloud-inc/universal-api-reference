# <img src="https://images.mindcloud.co/apps/icons/leap-ai_1775493959418.png" alt="Leap AI logo" width="28" height="28"> Leap AI: Universal API

Run published workflows and retrieve Leap workflow run results

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/leapAI/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://tryleap.ai
- **Vendor API docs:** https://docs.tryleap.ai/api-reference/getting-started

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Workflow Run](actions/get-workflow-run.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leapAI/latest/actions/get-workflow-run?connectionId=$CONNECTION_ID&workflowRunId=runv2_8R8jNYkpBVLI4FqCJiJ5" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Workflow Run

| Action | Method | Description |
| --- | --- | --- |
| [Get Workflow Run](actions/get-workflow-run.md) | GET | Retrieves a workflow run from Leap AI. |
| [Run Workflow](actions/run-workflow.md) | POST | Runs a published workflow in Leap AI. |

