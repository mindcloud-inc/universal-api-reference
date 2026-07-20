# <img src="https://images.mindcloud.co/apps/icons/favicon-docs-getfestivo-com-48x48_1777483116556.png" alt="Festivo logo" width="28" height="28"> Festivo: Universal API

Festivo provides a public holidays API for retrieving country holiday calendars, supported countries, regional observances, substitute holidays, and localized holiday metadata.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/festivo/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://getfestivo.com
- **Vendor API docs:** https://docs.getfestivo.com/docs/products/public-holidays-api/intro/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Available Countries](actions/list-available-countries.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/festivo/latest/actions/list-available-countries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Country

| Action | Method | Description |
| --- | --- | --- |
| [List Available Countries](actions/list-available-countries.md) | GET | Retrieves available country codes from Festivo. |

### Public Holiday

| Action | Method | Description |
| --- | --- | --- |
| [List Public Holidays](actions/list-public-holidays.md) | GET | Retrieves public holidays for a country and year from Festivo. |

