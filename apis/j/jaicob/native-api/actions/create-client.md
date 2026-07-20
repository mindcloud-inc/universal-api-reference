# Create Client with Jaicob

## Endpoint

- **Method:** `POST`
- **Path:** `/clients`
- **Base URL:** `https://api.jaicob.ai`
- **Official documentation:** [Create Client](https://developers.jaicob.ai/reference/create_client)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `companyName` | body | `string` | yes |
| `details` | body | `object` | no |
| `avatar` | body | `string` | no |
| `bannerImage` | body | `string` | no |
| `locationIds[]` | body | `array<string>` | no |
