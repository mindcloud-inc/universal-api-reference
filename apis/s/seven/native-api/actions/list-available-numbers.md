# List Available Numbers with Seven

Retrieves available numbers from Seven.

## Endpoint

- **Method:** `GET`
- **Path:** `/numbers/available`
- **Base URL:** `https://gateway.seven.io/api`
- **Official documentation:** [List Available Numbers](https://docs.seven.io/en/rest-api/endpoints/numbers#available-numbers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | query | `string` | no | The ISO 3166-1 alpha-2 country code of the country to search for available numbers in. |
| `features_sms` | query | `boolean` | no | If set to true , only numbers that support SMS will be returned. |
| `features_a2p_sms` | query | `boolean` | no | If set to true , only numbers that support A2P SMS will be returned. |
| `features_voice` | query | `boolean` | no | If set to true , only numbers that support voice will be returned. |
