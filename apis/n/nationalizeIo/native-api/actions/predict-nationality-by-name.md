# Predict Nationality by Name with Nationalize_io

Retrieves nationality predictions from Nationalize.io for one name.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://api.nationalize.io`
- **Official documentation:** [Predict Nationality by Name](https://nationalize.io/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | yes | Last name, first name, or full name to classify. Nationalize.io recommends using a last name when available. |
