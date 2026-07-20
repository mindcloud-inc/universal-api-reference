# Create Release with Cryptlex

Creates a release in Cryptlex.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/releases`
- **Base URL:** `https://api.cryptlex.com`
- **Official documentation:** [Create Release](https://api.cryptlex.com/v3/docs#tag/Releases/operation/post/v3/releases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel` | body | `string` | yes | Release channel. |
| `name` | body | `string` | yes | Release name. |
| `productId` | body | `string` | yes | Product linked to the release. |
| `version` | body | `string` | yes | Release version string. |
| `platforms[]` | body | `array<string>` | yes | Platforms supported by the release. |
