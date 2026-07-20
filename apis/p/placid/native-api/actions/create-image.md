# Create Image with Placid

Creates a new image in Placid from a template.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/rest/images`
- **Base URL:** `https://api.placid.app`
- **Official documentation:** [Create Image](https://placid.app/docs/2.0/rest/images#create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `template_uuid` | body | `string` | no |
| `webhook_success` | body | `string` | no |
| `create_now` | body | `boolean` | no |
| `passthrough` | body | `string` | no |
| `layers` | body | `object` | no |
| `transfer` | body | `object` | no |
| `modifications` | body | `object` | no |
