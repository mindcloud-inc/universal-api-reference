# Upload Profile File with Instafill

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/profiles/:profileId/files`
- **Base URL:** `https://api.instafill.ai`
- **Official documentation:** [Upload Profile File](https://api.instafill.ai/swagger)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `profileId` | path | `string` | yes |
| `files` | body | `list<file>` | yes |
| `textInfo` | body | `string` | no |
