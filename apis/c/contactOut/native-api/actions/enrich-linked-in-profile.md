# Enrich LinkedIn Profile with ContactOut

Retrieves profile details from a LinkedIn URL in ContactOut.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/linkedin/enrich`
- **Base URL:** `https://api.contactout.com`
- **Official documentation:** [Enrich LinkedIn Profile](https://api.contactout.com/#from-linkedin-url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profile` | query | `string` | yes | The full LinkedIn profile URL. |
