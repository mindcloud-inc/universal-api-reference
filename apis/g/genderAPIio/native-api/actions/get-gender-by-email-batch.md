# Get Gender by Email Batch with GenderAPI.io

Retrieves gender details from GenderAPI.io for multiple email addresses.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/email/multi/country`
- **Base URL:** `https://api.genderapi.io`
- **Official documentation:** [Get Gender by Email Batch](https://www.genderapi.io/docs-gender-from-email-multiple)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `list<object>` | yes | Array of email records to analyze. Each object can include email, country, and id. |
