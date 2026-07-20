# Batch Get LinkedIn Contact Info with ContactOut

Retrieves contact details for LinkedIn profiles in bulk from ContactOut.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/people/linkedin/batch`
- **Base URL:** `https://api.contactout.com`
- **Official documentation:** [Batch Get LinkedIn Contact Info](https://api.contactout.com/#v1-bulk-contactinfo)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profiles` | body | `string` | yes | An array of LinkedIn profile URLs. Send multiple values as a array. |
