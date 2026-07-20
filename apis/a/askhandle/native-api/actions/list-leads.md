# List Leads with AskHandle

Retrieves lead records from your AskHandle account.

## Endpoint

- **Method:** `GET`
- **Path:** `/leads/`
- **Base URL:** `https://dashboard.askhandle.com/api/v1`
- **Official documentation:** [List Leads](https://dashboard.askhandle.com/api/v1/docs/api_reference.html#lead)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `date` | no | Only return leads created on or after this date. |
| `end_date` | query | `date` | no | Only return leads created on or before this date. |
