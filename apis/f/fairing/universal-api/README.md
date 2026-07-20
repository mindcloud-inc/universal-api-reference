# <img src="https://images.mindcloud.co/apps/icons/fairing-icon-filled-256_1776780653941.png" alt="Fairing logo" width="28" height="28"> Fairing: Universal API

Fetch questions and response data from your Fairing account through the Fairing API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fairing/latest
- **Category:** Marketing
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://fairing.co
- **Vendor API docs:** https://docs.fairing.co/reference/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Questions](actions/list-questions.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fairing/latest/actions/list-questions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Question

| Action | Method | Description |
| --- | --- | --- |
| [List Questions](actions/list-questions.md) | GET | Retrieves questions from Fairing. |

### Response

| Action | Method | Description |
| --- | --- | --- |
| [List Responses](actions/list-responses.md) | GET | Retrieves responses from Fairing. |

