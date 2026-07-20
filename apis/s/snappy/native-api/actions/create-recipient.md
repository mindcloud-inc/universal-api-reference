# Create Recipient with Snappy

Creates a new recipient in Snappy.

## Endpoint

- **Method:** `POST`
- **Path:** `/recipients`
- **Base URL:** `https://api.snappy.com/public-api/v2`
- **Official documentation:** [Create Recipient](https://docs.snappy.com/reference/createrecipient)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accounts[]` | body | `array<string>` | yes |
| `companyId` | query | `string` | yes |
| `country` | body | `string` | yes |
| `firstName` | body | `string` | yes |
