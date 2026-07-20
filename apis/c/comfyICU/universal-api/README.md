# <img src="https://images.mindcloud.co/apps/icons/comfy-icu_1778253670055.png" alt="Comfy.ICU logo" width="28" height="28"> Comfy.ICU: Universal API

Run ComfyUI workflows on Comfy.ICU and retrieve run status and generated outputs through the Comfy.ICU REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/comfyICU/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://comfy.icu
- **Vendor API docs:** https://comfy.icu/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Run Status](actions/get-run-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/comfyICU/latest/actions/get-run-status?connectionId=$CONNECTION_ID&workflowId=6bAK1X_Y7QERnV30MZdo2&runId=APCmAT2lf8O6sAgk2Svf2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Workflow Run

| Action | Method | Description |
| --- | --- | --- |
| [Get Run Status](actions/get-run-status.md) | GET | Retrieves a workflow run status from Comfy.ICU. |
| [Run Workflow](actions/run-workflow.md) | POST | Creates a new workflow run in Comfy.ICU. |

