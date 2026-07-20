# <img src="https://images.mindcloud.co/apps/icons/companydatadk_1776081004402.png" alt="companydata.dk logo" width="28" height="28"> companydata.dk: Universal API

Search Danish companies, financials, and reference data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/companydatadk/latest
- **Category:** IT Operations / Database
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://companydata.dk
- **Vendor API docs:** https://api.companydata.dk/v1/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companydatadk/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves API key account details from companydata.dk. |

