# List CSV Uploads with IPQS Fraud and Risk Scoring

Retrieves uploaded CSV jobs from IPQS.

## Endpoint

- **Method:** `GET`
- **Path:** `/csv/list`
- **Base URL:** `https://www.ipqualityscore.com/api/json`
- **Official documentation:** [List CSV Uploads](https://www.ipqualityscore.com/documentation/csv-api/retrieve-csv-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `string` | no | Optional CSV type to list: proxy, email, url, or phone. |
| `page` | query | `number` | no | Page number of CSV uploads to return. |
