# Enrich Person With Personal Email with ContactOut

Retrieves a person's profile and personal email from ContactOut.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/people/enrich`
- **Base URL:** `https://api.contactout.com`
- **Official documentation:** [Enrich Person With Personal Email](https://api.contactout.com/#people-enrich-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `full_name` | body | `string` | no | Full name of the person to enrich. |
| `linkedin_url` | body | `string` | no | LinkedIn profile URL of the person. |
