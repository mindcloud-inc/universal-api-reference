# Create Business Object with PubNub

Creates a business object in PubNub Illuminate.

## Endpoint

- **Method:** `POST`
- **Path:** `/illuminate/business-objects`
- **Base URL:** `https://admin-api.pubnub.com/v2`
- **Official documentation:** [Create Business Object](https://www.pubnub.com/docs/illuminate/illuminate-rest-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Business object description. |
| `fields[0].jsonFieldType` | body | `string` | yes | Field type for the first field. |
| `fields[0].jsonPath` | body | `string` | yes | JSONPath for the first field. |
| `fields[0].name` | body | `string` | yes | Name for the first business object field. |
| `fields[0].source` | body | `string` | yes | Field source type for the first field. |
| `fields[1].jsonFieldType` | body | `string` | yes | Field type for the second field. |
| `fields[1].jsonPath` | body | `string` | yes | JSONPath for the second field. |
| `fields[1].name` | body | `string` | yes | Name for the second business object field. |
| `fields[1].source` | body | `string` | yes | Field source type for the second field. |
| `isActive` | body | `boolean` | yes | Whether the business object starts capturing data. |
| `name` | body | `string` | yes | Business object name. |
