# Enrich Person with ContactOut

Retrieves a person's profile from ContactOut using multiple identifiers.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/people/enrich`
- **Base URL:** `https://api.contactout.com`
- **Official documentation:** [Enrich Person](https://api.contactout.com/#people-enrich-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | body | `string` | no | Company name or names. |
| `email` | body | `string` | no | Email address of the person. |
| `full_name` | body | `string` | no | Full name of the person to enrich. |
| `linkedin_url` | body | `string` | no | LinkedIn profile URL of the person. |
| `include` | body | `string` | no | Optional contact data to include, such as work_email, personal_email, or phone. Send multiple values as a array. |
