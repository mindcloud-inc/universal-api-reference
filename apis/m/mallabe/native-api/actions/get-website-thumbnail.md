# Get Website Thumbnail with Mallabe

Retrieves a website thumbnail from Mallabe.

## Endpoint

- **Method:** `POST`
- **Path:** `/websites/thumbnail`
- **Base URL:** `https://mallabe.p.rapidapi.com/v1`
- **Official documentation:** [Get Website Thumbnail](https://app.mallabe.com/websites/thumbnail/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `website` | body | `string` | yes | Website URL to capture. |
| `webhookUrl` | body | `string` | no | Webhook URL for asynchronous callbacks. |
