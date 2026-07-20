# Search Orders with Amazon Seller

Finds orders in Amazon Seller by creation or update time.

## Endpoint

- **Method:** `GET`
- **Path:** `orders/2026-01-01/orders`
- **Base URL:** `https://{environment}-{region}.amazon.com`
- **API:** REST
- **Official documentation:** [Search Orders](https://developer-docs.amazon.com/sp-api/reference/searchorders)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `marketplaceIds` | query | `list<string>` | no | Find orders placed in only the marketplaces you select here. Accepted values: `A13V1IB3VIYZZH`, `A17E79C6D8DWNP`, `A1805IZSGTT6HS`, `A19VAU5U5O7RUS`, `A1AM78C64UM0Y8`, `A1C3SOZRARQ6R3`, `A1F83G8C2ARO7P`, `A1PA6795UKMFR9`, `A1RKKUPIHCS9HS`, `A1VC38T7YXB528`, `A21TJRUUN4KGV`, `A28R8C7NBKEWEA`, `A2EUQ1WTGCTBG2`, `A2NODRKZP88ZB9`, `A2Q3Y263D00KWC`, `A2VIGQ35RCS4UG`, `A33AVAJ2PDY3EV`, `A39IBJ37TRP1C6`, `AE08WJ6YKNBMC`, `AMEN7PMS3EDWL`, `APJ6JRA9NG5V4`, `ARBP9OOSHTCHU`, `ATVPDKIKX0DER`. Maximum length: 50. Send multiple values as a string. |
| `includedData` | query | `list<string>` | no | A list of datasets to include in the response. Send multiple values as a array. |
| `fulfilledBy` | query | `list<string>` | no | The response includes orders that are fulfilled by the parties that you choose. When nothing is selected all are returned. Send multiple values as a array. |
| `fulfillmentStatuses` | query | `list<string>` | no | Choose one or more statuses to filter the results. Send multiple values as a array. |
| `createdAfter` | query | `date` | no | — |
| `createdBefore` | query | `string` | no | — |
| `lastUpdatedAfter` | query | `string` | no | — |
| `lastUpdatedBefore` | query | `string` | no | — |
