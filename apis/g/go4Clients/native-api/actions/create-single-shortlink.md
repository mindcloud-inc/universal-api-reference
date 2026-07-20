# Create Single Shortlink with Go4Clients

Creates a shortlink without a campaign in Go4Clients.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/campaigns/shortlink/v1.0/single`
- **Base URL:** `https://cloud.go4clients.com:8580`
- **Official documentation:** [Create Single Shortlink](https://apidoc.go4clients.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | body | `string` | yes | Shortlink key. |
| `expirationDays` | body | `number` | yes | How many days the shortlink remains active. |
| `type` | body | `string` | yes | Shortlink target type: URL or LANDING. |
| `url` | body | `string` | no | Target URL when type is URL. |
| `landingId` | body | `string` | no | Landing identifier when type is LANDING. |
