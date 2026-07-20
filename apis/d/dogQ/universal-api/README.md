# <img src="https://images.mindcloud.co/apps/icons/dog-q_1775827896058.png" alt="DogQ logo" width="28" height="28"> DogQ: Universal API

Run DogQ tests, manage webhooks, and inspect execution results

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dogQ/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://dogq.io
- **Vendor API docs:** https://docs.dogq.io/documentation/integrations

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Run Project](actions/run-project.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dogQ/latest/actions/run-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

## Actions (1)

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Run Project](actions/run-project.md) | POST | Runs a DogQ project with optional variables and contexts. |

