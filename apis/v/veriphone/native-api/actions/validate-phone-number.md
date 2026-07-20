# Validate Phone Number with Veriphone

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/verify`
- **Base URL:** `https://api.veriphone.io`
- **Official documentation:** [Validate Phone Number](https://veriphone.io/docs/v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phone` | query | `string` | yes | Phone number to validate |
| `default_country` | query | `string` | no | Default country code |
