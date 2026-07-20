# Get Suppression with UniOne

Retrieves suppression details from UniOne by email address.

## Endpoint

- **Method:** `POST`
- **Path:** `suppression/get.json`
- **Base URL:** `https://api.unione.io/en/transactional/api/v1`
- **Official documentation:** [Get Suppression](https://docs.unione.io/en/web-api-ref#suppression-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address to look up in the suppression list. |
| `all_projects` | body | `boolean` | no | Whether to search across all projects for this email. |
