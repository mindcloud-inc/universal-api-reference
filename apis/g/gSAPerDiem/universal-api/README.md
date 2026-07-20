# GSA Per Diem: Universal API

Retrieve official GSA continental U.S. per diem lodging and meals and incidental expense rates by city, state, ZIP code, or fiscal year.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/gSAPerDiem/latest
- **Category:** Business Intelligence / Data Warehouse
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.gsa.gov/travel/plan-a-trip/per-diem-rates
- **Vendor API docs:** https://open.gsa.gov/api/perdiem/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List CONUS M&IE Breakdown Rates](actions/list-conus-mie-breakdown-rates.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gSAPerDiem/latest/actions/list-conus-mie-breakdown-rates?connectionId=$CONNECTION_ID&year=2026" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Per Diem Rates by City](actions/get-per-diem-rates-by-city.md) | GET | Retrieves per diem rates from GSA Per Diem by city. |
| [Get Per Diem Rates by ZIP Code](actions/get-per-diem-rates-by-zip-code.md) | GET | Retrieves per diem rates from GSA Per Diem by ZIP code. |
| [List CONUS Lodging Rates](actions/list-conus-lodging-rates.md) | GET | Retrieves CONUS lodging rates from GSA Per Diem. |
| [List CONUS M&IE Breakdown Rates](actions/list-conus-mie-breakdown-rates.md) | GET | Retrieves CONUS M&IE breakdown rates from GSA Per Diem. |
| [List CONUS ZIP Code Destination IDs](actions/list-conus-zip-code-destination-ids.md) | GET | Retrieves CONUS ZIP code destination IDs from GSA Per Diem. |
| [List Per Diem Rates by State](actions/list-per-diem-rates-by-state.md) | GET | Retrieves per diem rates from GSA Per Diem by state. |

