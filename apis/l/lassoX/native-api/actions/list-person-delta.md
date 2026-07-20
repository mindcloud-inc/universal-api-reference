# List Person Delta with Lasso X

Retrieves changed people from Lasso X since a given date.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/cvr/person/delta`
- **Base URL:** `https://api.lassox.com`
- **Official documentation:** [List Person Delta](https://docs.lassox.com/data-apis/cvr/#getting-changes-delta)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `since` | query | `date` | yes | Start date for delta search, e.g. 2021-02-01. |
| `max` | query | `date` | no | Maximum date for delta search. |
| `pageSize` | query | `number` | no | Number of results to return. |
