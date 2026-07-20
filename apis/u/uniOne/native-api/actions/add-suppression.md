# Add Suppression with UniOne

Adds an email address to UniOne's suppression list.

## Endpoint

- **Method:** `POST`
- **Path:** `suppression/set.json`
- **Base URL:** `https://api.unione.io/en/transactional/api/v1`
- **Official documentation:** [Add Suppression](https://docs.unione.io/en/web-api-ref#suppression-set)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address to add to the suppression list. |
| `cause` | body | `string` | yes | Reason for suppression. |
