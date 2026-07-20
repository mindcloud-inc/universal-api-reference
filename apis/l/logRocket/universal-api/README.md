# <img src="https://images.mindcloud.co/apps/icons/favicon-docs-logrocket-com-48x48_1778074164408.png" alt="LogRocket logo" width="28" height="28"> LogRocket: Universal API

LogRocket provides session replay, product analytics, issue tracking, and Galileo AI summaries for web and mobile application behavior.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/logRocket/latest
- **Category:** IT Operations / Observability
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://logrocket.com
- **Vendor API docs:** https://docs.logrocket.com/docs/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Highlights Result](actions/get-highlights-result.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logRocket/latest/actions/get-highlights-result?connectionId=$CONNECTION_ID&id=highlights%20request%20id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Highlights Result](actions/get-highlights-result.md) | GET |  |
| [Request User Highlights](actions/request-user-highlights.md) | POST |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Update User Information](actions/update-user-information.md) | PUT |  |

