# Get LinkedIn Contact Info with ContactOut

Retrieves contact details for a LinkedIn profile from ContactOut.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/people/linkedin`
- **Base URL:** `https://api.contactout.com`
- **Official documentation:** [Get LinkedIn Contact Info](https://api.contactout.com/#from-linkedin-profile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_phone` | query | `string` | no | Set to true to request phone data. |
| `profile` | query | `string` | yes | The full LinkedIn profile URL. |
