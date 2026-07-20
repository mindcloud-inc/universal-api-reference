# Update Client with Jaicob

## Endpoint

- **Method:** `PUT`
- **Path:** `/clients/[:id]`
- **Base URL:** `https://api.jaicob.ai`
- **Official documentation:** [Update Client](https://developers.jaicob.ai/reference/update_client)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Client identifier. |
| `companyName` | body | `string` | no | — |
| `details` | body | `object` | no | — |
| `avatar` | body | `string` | no | — |
| `bannerImage` | body | `string` | no | — |
| `userId` | body | `string` | no | — |
| `ownerLocationIds[]` | body | `array<string>` | no | — |
