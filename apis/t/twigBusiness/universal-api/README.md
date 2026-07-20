# <img src="https://images.mindcloud.co/apps/icons/twig-business_1775823244586.png" alt="Twig Business logo" width="28" height="28"> Twig Business: Universal API

Create Twig agents, connect data sources, and query knowledge bases

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/twigBusiness/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.twig.so
- **Vendor API docs:** https://help.twig.so/product/developer-api/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Lambda Logs](actions/get-lambda-logs.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twigBusiness/latest/actions/get-lambda-logs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Get Lambda Logs](actions/get-lambda-logs.md) | GET |  |
| [Get Process Logs](actions/get-process-logs.md) | GET |  |
| [List Data Sources](actions/list-data-sources.md) | GET |  |
| [List Subscriptions](actions/list-subscriptions.md) | GET |  |
| [Search Data Sources](actions/search-data-sources.md) | GET |  |

