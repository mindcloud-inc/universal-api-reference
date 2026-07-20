# Detect Language From HTML Fragment via HTTP GET with Dandelion

Retrieves detected languages from an HTML fragment in Dandelion via HTTP GET.

## Endpoint

- **Method:** `GET`
- **Path:** `/datatxt/li/v1`
- **Base URL:** `https://api.dandelion.eu`
- **Official documentation:** [Detect Language From HTML Fragment via HTTP GET](https://dandelion.eu/docs/api/datatxt/li/v1/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `html_fragment` | query | `string` | yes | HTML Fragment to analyze. |
| `clean` | query | `boolean` | no | Clean URLs, email addresses, hashtags, and more before analysis. |
