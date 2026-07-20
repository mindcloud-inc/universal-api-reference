# Create Client with Uku

Creates a new client in Uku.

## Endpoint

- **Method:** `POST`
- **Path:** `/clients`
- **Base URL:** `https://app.getuku.com/api/v1.0`
- **Official documentation:** [Create Client](https://app.getuku.com/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address_country_code` | body | `string` | yes | ISO country code |
| `client_initials` | body | `string` | yes | Client initials |
| `name` | body | `string` | yes | Client name |
