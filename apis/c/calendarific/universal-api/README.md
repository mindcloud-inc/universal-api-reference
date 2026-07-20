# <img src="https://images.mindcloud.co/apps/icons/calendarific_1777493216911.png" alt="Calendarific logo" width="28" height="28"> Calendarific: Universal API

Calendarific provides worldwide holiday and observance data across countries, states, regions, and languages.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/calendarific/latest
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://calendarific.com/
- **Vendor API docs:** https://calendarific.com/api-documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Countries](actions/list-countries.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calendarific/latest/actions/list-countries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Country

| Action | Method | Description |
| --- | --- | --- |
| [List Countries](actions/list-countries.md) | GET | Retrieves supported countries from Calendarific. |

### Holiday

| Action | Method | Description |
| --- | --- | --- |
| [List Holidays](actions/list-holidays.md) | GET | Retrieves holidays from Calendarific by country and year. |

### Language

| Action | Method | Description |
| --- | --- | --- |
| [List Languages](actions/list-languages.md) | GET | Retrieves supported languages from Calendarific. |

