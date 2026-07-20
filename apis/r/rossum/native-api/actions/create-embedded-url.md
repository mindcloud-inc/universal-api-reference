# Create Embedded URL with Rossum

Creates an embedded URL for an annotation in Rossum.

## Endpoint

- **Method:** `POST`
- **Path:** `/annotations/:annotationID/create_embedded_url`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [Create Embedded URL](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `annotationID` | path | `number` | yes |
| `return_url` | body | `string` | no |
| `cancel_url` | body | `string` | no |
| `delete_url` | body | `string` | no |
| `postpone_url` | body | `string` | no |
| `max_token_lifetime_s` | body | `number` | no |
