# Enrich Email with ContactOut

Retrieves profile details from an email address in ContactOut.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/email/enrich`
- **Base URL:** `https://api.contactout.com`
- **Official documentation:** [Enrich Email](https://api.contactout.com/#from-email-address)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | The email address to enrich. |
| `include` | query | `string` | no | Optional extra data to return. ContactOut currently supports work_email. |
