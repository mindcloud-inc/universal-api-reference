# Create File with Eledo

Creates a new file in Eledo.

## Endpoint

- **Method:** `POST`
- **Path:** `/CreateFile`
- **Base URL:** `https://eledo.online/api/RESTv1`
- **Official documentation:** [Create File](https://eledo.online/documentation/api_reference/create_file)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `templateId` | body | `string` | yes |
| `templateVersion` | body | `number` | no |
| `file` | body | `object` | no |
| `temporary` | body | `boolean` | no |
