# Get multiple tags with Asana

Retrieves tags from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `tags`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get multiple tags](https://developers.asana.com/reference/gettags)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `opt_pretty` | query | `boolean` | no |
| `workspace` | query | `string` | no |
| `opt_fields` | query | `list<string>` | no |
