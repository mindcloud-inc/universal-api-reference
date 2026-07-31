# Predict Age with Agify

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://api.agify.io`
- **Official documentation:** [Predict Age](https://agify.io/documentation/api/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | yes | First or full name to use for the age prediction. |
| `country_id` | query | `string` | no | Optional ISO 3166-1 alpha-2 country code to scope the prediction. Maximum length: 2. |
