# Search Contacts with Lusha Connect

Finds contacts in Lusha Connect by enrichment inputs.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/person`
- **Base URL:** `https://api.lusha.com`
- **Official documentation:** [Search Contacts](https://docs.lusha.com/apis/openapi/enrichment/searchsinglecontact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contacts` | body | `list<object>` | yes | List of contact lookup objects. Each item must include contactId and one supported lookup combination such as email, linkedinUrl, or fullName with companies. |
