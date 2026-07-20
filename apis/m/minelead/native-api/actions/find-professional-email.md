# Find Professional Email with Minelead

Finds a professional email in Minelead by name and domain.

## Endpoint

- **Method:** `GET`
- **Path:** `/find`
- **Base URL:** `https://api.minelead.io/v1`
- **Official documentation:** [Find Professional Email](https://api.minelead.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | yes | Company domain for the person lookup. |
| `firstname` | query | `string` | yes | Person's first name. |
| `lastname` | query | `string` | yes | Person's last name. |
