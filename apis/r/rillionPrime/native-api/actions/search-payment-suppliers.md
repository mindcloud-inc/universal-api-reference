# Search Payment Suppliers with Rillion Prime Pay

## Endpoint

- **Method:** `GET`
- **Path:** `/payment/supplier/typeahead`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Search Payment Suppliers](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | yes | Search term used to find suppliers. |
| `limit` | query | `number` | no | Maximum number of supplier results to return. |
