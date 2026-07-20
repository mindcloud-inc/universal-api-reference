# Get CSV Status And Download Links with IPQS Fraud and Risk Scoring

Retrieves CSV processing status and download links from IPQS.

## Endpoint

- **Method:** `GET`
- **Path:** `/csv/{apiKey}/status/:csvId`
- **Base URL:** `https://www.ipqualityscore.com/api/json`
- **Official documentation:** [Get CSV Status And Download Links](https://www.ipqualityscore.com/documentation/csv-api/check-csv-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `csvId` | path | `number` | yes | CSV ID returned by a prior upload. |
