# <img src="https://images.mindcloud.co/apps/icons/icon_1774982468088.png" alt="Gusto logo" width="28" height="28"> Gusto: Universal API

Gusto payroll and HR data for companies, employees, payrolls, contractors, benefits, reports, and time tracking.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/gusto/latest
- **Category:** Human Resources / HRIS
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://docs.gusto.com/app-integrations/docs
- **Vendor API docs:** https://docs.gusto.com/app-integrations/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Token Info](actions/get-token-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gusto/latest/actions/get-token-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Token Info

| Action | Method | Description |
| --- | --- | --- |
| [Get Token Info](actions/get-token-info.md) | GET | Retrieves OAuth token information from Gusto. |

