# Reverse Lookup Domain with Clearout

Retrieves company lead information from Clearout by domain.

## Endpoint

- **Method:** `GET`
- **Path:** `/reverse_lookup/domain`
- **Base URL:** `https://api.clearout.io/v2`
- **Official documentation:** [Reverse Lookup Domain](https://docs.clearout.io/developers/api/reverse-lookup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | yes | Domain name to lookup |
