# Search Transactions with Viewpoint Vista

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/{subscriberCode}/vista/ar/2/data/transactions/cache/search`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Search Transactions](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistaar2datatransactionscachesearchsearch)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modifiedUtcAfter` | body | `date` | no | Returns transactions modified after this timestamp. Format: yyyy-MM-ddThh:mm:ss.fffffffZ. |
| `modifiedUtcBefore` | body | `date` | no | Returns transactions modified before this timestamp. Format: yyyy-MM-ddThh:mm:ss.fffffffZ. |
