# <img src="https://images.mindcloud.co/apps/icons/u-kbank-holidays_1777929057678.png" alt="UK Bank Holidays logo" width="28" height="28"> UK Bank Holidays: Universal API

Official UK government bank holiday dates for England and Wales, Scotland, and Northern Ireland.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/uKBankHolidays/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.gov.uk/bank-holidays
- **Vendor API docs:** https://www.api.gov.uk/gds/bank-holidays/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Bank Holidays](actions/list-bank-holidays.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uKBankHolidays/latest/actions/list-bank-holidays?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Bank Holiday

| Action | Method | Description |
| --- | --- | --- |
| [List Bank Holidays](actions/list-bank-holidays.md) | GET | Retrieves UK bank holiday dates from UK Bank Holidays. |

