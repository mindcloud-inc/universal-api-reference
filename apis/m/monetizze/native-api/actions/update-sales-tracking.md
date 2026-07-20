# Update Sales Tracking with Monetizze

Updates sales tracking codes in Monetizze.

## Endpoint

- **Method:** `POST`
- **Path:** `/sales/tracking`
- **Base URL:** `https://api.monetizze.com.br/2.1`
- **Official documentation:** [Update Sales Tracking](https://api.monetizze.com.br/2.1/apidoc/#api-Produtor-Tracking)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `string` | yes | JSON array string with objects like [{"codLog":1,"transaction":1,"trackingCode":"PA123456789BR"}]. |
