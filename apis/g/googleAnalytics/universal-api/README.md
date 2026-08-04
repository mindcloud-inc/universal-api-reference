# <img src="https://images.mindcloud.co/apps/icons/como-criar-uma-propriedade-do-google-analytics-4_1758304207339.png" alt="Google Analytics logo" width="28" height="28"> Google Analytics: Universal API

Google Analytics through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/googleAnalytics/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Account Summaries](actions/list-account-summaries.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAnalytics/latest/actions/list-account-summaries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Other

| Action | Method | Description |
| --- | --- | --- |
| [List Account Summaries](actions/list-account-summaries.md) | GET |  |
| [List Accounts](actions/list-accounts.md) | GET |  |

