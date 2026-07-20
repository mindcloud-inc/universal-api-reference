# Reverse Lookup Email Address with Clearout

Retrieves lead information from Clearout by email address.

## Endpoint

- **Method:** `GET`
- **Path:** `/reverse_lookup/email`
- **Base URL:** `https://api.clearout.io/v2`
- **Official documentation:** [Reverse Lookup Email Address](https://docs.clearout.io/developers/api/reverse-lookup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email_address` | query | `string` | yes | Email address to lookup |
