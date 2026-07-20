# Search Clients with Intradesk

Finds clients in Intradesk by email or phone.

## Endpoint

- **Method:** `GET`
- **Path:** `/settings/api/v1/clients/Search`
- **Base URL:** `https://apigw.intradesk.ru`
- **Official documentation:** [Search Clients](https://apigw.intradesk.ru/settings_docs/swagger/index.html#/Clients/get_api_v1_clients_Search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Client email search filter. |
| `phone` | query | `string` | no | Client phone search filter. |
| `top` | query | `number` | no | Maximum number of clients to return. Defaults to 50 in Intradesk docs. |
| `isIncludeArchived` | query | `boolean` | no | Whether archived clients should be included. Defaults to false in Intradesk docs. |
