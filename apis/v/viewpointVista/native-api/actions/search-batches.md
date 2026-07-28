# Search Batches with Viewpoint Vista

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/{subscriberCode}/vista/ar/2/data/batches/cache/search`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Search Batches](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistaar2databatchescachesearchsearch)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modifiedUtcAfter` | body | `date` | no | Returns batches modified after this timestamp. Format: yyyy-MM-ddThh:mm:ss.fffffffZ. |
| `modifiedUtcBefore` | body | `date` | no | Returns batches modified before this timestamp. Format: yyyy-MM-ddThh:mm:ss.fffffffZ. |
