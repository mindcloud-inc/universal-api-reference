# Create Profile with ProvenExpert

Creates a profile in ProvenExpert.

## Endpoint

- **Method:** `POST`
- **Path:** `/profile/create`
- **Base URL:** `https://www.provenexpert.com/api/v1`
- **Official documentation:** [Create Profile](https://developer.provenexpert.com/index_en.html#profile-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.email` | body | `string` | yes | Email address for the new profile. |
| `data.company` | body | `string` | yes | Company name for the new company profile. |
| `data.description` | body | `string` | no | Optional profile description. |
