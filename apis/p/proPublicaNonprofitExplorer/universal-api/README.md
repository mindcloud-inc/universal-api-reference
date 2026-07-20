# <img src="https://images.mindcloud.co/apps/icons/pro-publica-nonprofit-explorer_1777481396059.png" alt="ProPublica Nonprofit Explorer logo" width="28" height="28"> ProPublica Nonprofit Explorer: Universal API

Search and inspect nonprofit tax-return records

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/proPublicaNonprofitExplorer/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://projects.propublica.org/nonprofits/
- **Vendor API docs:** https://projects.propublica.org/nonprofits/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Organization](actions/get-organization.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proPublicaNonprofitExplorer/latest/actions/get-organization?connectionId=$CONNECTION_ID&ein=142007220" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET | Retrieves an organization from ProPublica Nonprofit Explorer by EIN. |
| [Search Organizations](actions/search-organizations.md) | GET | Finds organizations in ProPublica Nonprofit Explorer. |

