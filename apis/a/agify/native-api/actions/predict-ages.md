# Predict Ages with Agify

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://api.agify.io`
- **Official documentation:** [Predict Ages](https://agify.io/documentation/api/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name[]` | query | `array<string>` | yes | Up to 10 names to predict in one request. Maximum length: 10. Send multiple values as a array. |
| `country_id` | query | `string` | no | Optional ISO 3166-1 alpha-2 country code to scope every prediction in the batch. Maximum length: 2. |
