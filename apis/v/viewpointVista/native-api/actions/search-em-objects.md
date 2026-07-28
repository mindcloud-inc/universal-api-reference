# Search EM Objects with Viewpoint Vista

Search data found in Viewpoint® Vista™ Equipment Management ( EM ) programs.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache/search`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Search EM Objects](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modifiedUtcAfter` | body | `date` | no | — |
| `modifiedUtcBefore` | body | `date` | no | — |
| `object` | path | `list<string>` | yes | Specify the type of Object from the Equipment Management V2 Direct API that you'd like to retrieve. |
