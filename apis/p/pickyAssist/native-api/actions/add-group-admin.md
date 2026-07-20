# Add Group Admin with Picky Assist

## Endpoint

- **Method:** `POST`
- **Path:** `/add-group-admin`
- **Base URL:** `https://app.pickyassist.com/api/v2`
- **Official documentation:** [Add Group Admin](https://help.pickyassist.com/api-documentation-v2/postman-collection-for-picky-assist-apis)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `group_id` | body | `string` | yes |
| `number[]` | body | `array<string>` | yes |
