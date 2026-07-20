# Validate Fax Number with Documo

Validates a fax number in Documo.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/numbers/validate`
- **Base URL:** `https://api.documo.com`
- **Official documentation:** [Validate Fax Number](https://docs.documo.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number` | query | `string` | yes | The fax number to validate. |
| `country` | query | `string` | yes | The alpha-2 country code for the number. |
