# Update Profile with Late

## Endpoint

- **Method:** `PUT`
- **Path:** `/profiles/:profileId`
- **Base URL:** `https://zernio.com/api/v1`
- **Official documentation:** [Update Profile](https://docs.zernio.com/profiles/update-profile)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `profileId` | path | `string` | yes |
| `name` | body | `string` | no |
| `description` | body | `string` | no |
| `color` | body | `string` | no |
| `isDefault` | body | `boolean` | no |
