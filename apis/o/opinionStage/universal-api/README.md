# <img src="https://images.mindcloud.co/apps/icons/opinion-stage_1774535615971.png" alt="Opinion Stage logo" width="28" height="28"> Opinion Stage: Universal API

Retrieve Opinion Stage items, questions, responses, and verified widget-runtime interactions.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/opinionStage/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.opinionstage.com/
- **Vendor API docs:** https://api.opinionstage.com/api-docs/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Items](actions/list-items.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/opinionStage/latest/actions/list-items?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Item

| Action | Method | Description |
| --- | --- | --- |
| [List Items](actions/list-items.md) | GET | Retrieves a list of items from Opinion Stage. |

