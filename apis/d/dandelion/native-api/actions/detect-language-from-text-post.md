# Detect Language From Text via HTTP POST with Dandelion

Retrieves detected languages from text in Dandelion via HTTP POST.

## Endpoint

- **Method:** `POST`
- **Path:** `/datatxt/li/v1`
- **Base URL:** `https://api.dandelion.eu`
- **Official documentation:** [Detect Language From Text via HTTP POST](https://dandelion.eu/docs/api/datatxt/li/v1/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | query | `string` | yes | Text to analyze. |
| `clean` | query | `boolean` | no | Clean URLs, email addresses, hashtags, and more before analysis. |
