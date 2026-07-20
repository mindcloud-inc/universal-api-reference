# <img src="https://images.mindcloud.co/apps/icons/zillow-public-records_1776963970949.png" alt="Zillow Public Records logo" width="28" height="28"> Zillow Public Records: Universal API

Bridge-hosted Zillow Public Records access. Requires a Bridge account plus approved public-records datasets/databases.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zillowPublicRecords/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.zillowgroup.com/developers/api/public-data/public-records-api/
- **Vendor API docs:** https://bridgedataoutput.com/docs/platform

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List assessments](actions/list-assessments.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zillowPublicRecords/latest/actions/list-assessments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [List parcel transactions](actions/list-parcel-transactions.md) | GET | Retrieves parcel transactions from Zillow Public Records by parcel ID. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [List assessments](actions/list-assessments.md) | GET | Retrieves public property assessments from Zillow Public Records. |

