# Search Potential Projects with Viewpoint Vista

Search Potential Project objects in Viewpoint® Vista™.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache/search`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Search Potential Projects](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `modifiedUtcAfter` | body | `date` | no |
| `modifiedUtcBefore` | body | `date` | no |
