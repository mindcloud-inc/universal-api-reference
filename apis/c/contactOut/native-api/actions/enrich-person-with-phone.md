# Enrich Person With Phone with ContactOut

Retrieves a person's profile and phone from ContactOut.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/people/enrich`
- **Base URL:** `https://api.contactout.com`
- **Official documentation:** [Enrich Person With Phone](https://api.contactout.com/#people-enrich-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `full_name` | body | `string` | no | Full name of the person to enrich. |
| `linkedin_url` | body | `string` | no | LinkedIn profile URL of the person. |
