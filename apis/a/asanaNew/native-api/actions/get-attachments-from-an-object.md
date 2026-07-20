# Get attachments from an object with Asana

Retrieves attachments for an object from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `attachments`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get attachments from an object](https://developers.asana.com/reference/getattachmentsforobject)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `opt_pretty` | query | `boolean` | no |
| `parent` | query | `string` | yes |
| `opt_fields` | query | `list<string>` | no |
