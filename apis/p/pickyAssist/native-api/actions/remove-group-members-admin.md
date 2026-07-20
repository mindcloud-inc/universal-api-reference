# Remove Group Members / Admin with Picky Assist

## Endpoint

- **Method:** `POST`
- **Path:** `/remove-group-members`
- **Base URL:** `https://app.pickyassist.com/api/v2`
- **Official documentation:** [Remove Group Members / Admin](https://help.pickyassist.com/api-documentation-v2/postman-collection-for-picky-assist-apis)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `group_id` | body | `string` | yes |
| `type` | body | `number` | yes |
| `number[]` | body | `array<string>` | yes |
