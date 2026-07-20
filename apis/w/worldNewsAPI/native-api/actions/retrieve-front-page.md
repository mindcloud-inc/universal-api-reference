# Retrieve Front Page with World News API

Retrieves a newspaper front page from World News API.

## Endpoint

- **Method:** `GET`
- **Path:** `/retrieve-front-page`
- **Base URL:** `https://api.worldnewsapi.com`
- **Official documentation:** [Retrieve Front Page](https://worldnewsapi.com/docs/newspaper-front-pages/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `date` | no | Date of the newspaper front page to retrieve. |
| `source-country` | query | `string` | no | Two-letter country code for the front page source. |
| `source-name` | query | `string` | no | Provider source name for the newspaper front page. |
