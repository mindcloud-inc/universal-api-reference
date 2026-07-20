# Get Message with Listrak Email

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/List/:listID/Message/:messageID`
- **Base URL:** `https://api.listrak.com/email`
- **Official documentation:** [Get Message](https://api.listrak.com/email#tag/List)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `listID` | path | `string` | yes |
| `messageID` | path | `string` | yes |
