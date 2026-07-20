# <img src="https://images.mindcloud.co/apps/icons/abstract-api-favicon_1777394869288.png" alt="Abstract Holidays logo" width="28" height="28"> Abstract Holidays: Universal API

Retrieve public, local, religious, and other holidays for a country using Abstract's Public Holidays API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/abstractHolidays/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.abstractapi.com/api/holidays-api
- **Vendor API docs:** https://docs.abstractapi.com/api/holidays

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Holidays](actions/get-holidays.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/abstractHolidays/latest/actions/get-holidays?connectionId=$CONNECTION_ID&country=US" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Holiday

| Action | Method | Description |
| --- | --- | --- |
| [Get Holidays](actions/get-holidays.md) | GET | Retrieves holidays from Abstract Holidays for a country and date. |

