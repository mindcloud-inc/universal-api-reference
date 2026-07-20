# Upload an attachment with Asana

Uploads an attachment to an object in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `attachments`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Upload an attachment](https://developers.asana.com/reference/createattachmentforobject)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `connect_to_app` | body | `boolean` | yes |
| `file` | body | `string` | yes |
| `name` | body | `string` | yes |
| `opt_pretty` | query | `boolean` | no |
| `parent` | body | `string` | yes |
| `resource_subtype` | body | `string` | yes |
| `url` | body | `string` | yes |
| `opt_fields` | query | `list<string>` | no |
