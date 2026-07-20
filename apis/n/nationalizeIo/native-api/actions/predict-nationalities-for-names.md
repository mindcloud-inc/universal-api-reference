# Predict Nationalities for Names with Nationalize_io

Retrieves nationality predictions from Nationalize.io for up to 10 names.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://api.nationalize.io`
- **Official documentation:** [Predict Nationalities for Names](https://nationalize.io/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name[]` | query | `array<string>` | yes | Names to classify in one request. Nationalize.io supports up to 10 names per batch using repeated name[] query parameters. Send multiple values as a array. |
