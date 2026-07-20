# Query with QuickBooks Online

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://:quickbooksEnvironment/v3/company/:realmId`
- **Official documentation:** [Query](https://developer.intuit.com/app/developer/qbo/docs/learn/explore-the-quickbooks-online-api/data-queries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | QuickBooks SQL-like query string, for example select * from Customer. |
