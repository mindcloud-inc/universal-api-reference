# Search AP Objects with Viewpoint Vista

Search objects found in the Viewpoint® Vista™ Accounts Payable (AP) programs.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache/search`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Search AP Objects](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modifiedUtcAfter` | body | `date` | no | Specify a datetime against which to filter the results. |
| `modifiedUtcBefore` | body | `date` | no | Specify a datetime against which to filter the results. |
| `object` | path | `list<string>` | yes | Specify the type of Object from the Accounts Payable V2 Direct API that you'd like to retrieve. |
