# Suggest Destinations with Airlabs

Finds destination suggestions in Airlabs by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/suggest`
- **Base URL:** `https://airlabs.co/api/v9`
- **Official documentation:** [Suggest Destinations](https://airlabs.co/docs/suggest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Part of the destination name, airport, city, or country. AirLabs documents 3 to 30 characters. Maximum length: 30. |
