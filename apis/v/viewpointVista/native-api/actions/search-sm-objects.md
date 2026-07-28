# Search SM Objects with Viewpoint Vista

Search data found in Viewpoint® Vista™ Service Management ( SM ) programs.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache/search`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Search SM Objects](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modifiedUtcAfter` | body | `date` | no | Returns objects that were modified after the specified date (ISO 8601 format).  Format: `yyyy-MM-ddThh:mm:ss.fffffffZ`. Example `2019-12-11T20:16:58.3419275Z`. |
| `object` | path | `list<string>` | yes | Specify the type of Object from the Service Management V2 Direct API that you'd like to retrieve. |
| `modifiedUtcBefore` | body | `date` | no | Returns objects that were modified before the specified date (ISO 8601 format).  Format: `yyyy-MM-ddThh:mm:ss.fffffffZ`. Example `2019-12-11T20:16:58.3419275Z`. |
