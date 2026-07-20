# Check Reply with JustCall

Checks for a reply in JustCall.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2.1/texts/checkreply`
- **Base URL:** `https://api.justcall.io`
- **Official documentation:** [Check Reply](https://developer.justcall.io/reference/texts_checkreply_v21)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contact_number` | body | `string` | yes |
| `justcall_number` | body | `string` | no |
