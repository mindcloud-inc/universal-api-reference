# Number Lookup with Go4Clients

Retrieves phone number lookup details from Go4Clients.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/lookup/v1.0/{{phoneNumber}}`
- **Base URL:** `https://cloud.go4clients.com:8580`
- **Official documentation:** [Number Lookup](https://apidoc.go4clients.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phoneNumber` | path | `string` | yes | Phone number including country code. |
