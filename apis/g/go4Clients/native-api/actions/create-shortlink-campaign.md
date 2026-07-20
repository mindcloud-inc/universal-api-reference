# Create Shortlink Campaign with Go4Clients

Creates a new shortlink campaign in Go4Clients.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/campaigns/shortlink/v1.0`
- **Base URL:** `https://cloud.go4clients.com:8580`
- **Official documentation:** [Create Shortlink Campaign](https://apidoc.go4clients.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the shortlink campaign. |
| `programId` | body | `string` | yes | Program identifier the campaign belongs to. |
| `expirationDays` | body | `number` | yes | How many days the shortlink remains available. |
| `description` | body | `string` | no | Optional shortlink campaign description. |
| `input` | body | `object` | yes | Shortlink input object with type and either baseUrl or landing details. |
