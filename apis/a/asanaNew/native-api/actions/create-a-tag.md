# Create a tag with Asana

Creates a tag in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `tags`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Create a tag](https://developers.asana.com/reference/createtag)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data` | body | `string` | yes |
| `opt_pretty` | query | `boolean` | no |
| `opt_fields` | query | `list<string>` | no |
