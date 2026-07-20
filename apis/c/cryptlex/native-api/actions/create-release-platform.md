# Create Release Platform with Cryptlex

Creates a release platform in Cryptlex.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/release-platforms`
- **Base URL:** `https://api.cryptlex.com`
- **Official documentation:** [Create Release Platform](https://api.cryptlex.com/v3/docs#tag/ReleasePlatforms/operation/post/v3/release-platforms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Platform name. |
| `displayName` | body | `string` | yes | Platform display name. |
| `description` | body | `string` | no | Platform description. |
| `productIds[]` | body | `array<string>` | no | Product IDs to associate with the release platform. Send multiple values as a array. |
