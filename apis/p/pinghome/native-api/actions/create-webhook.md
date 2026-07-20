# Create Webhook with Pinghome

Creates a new webhook in Pinghome.

## Endpoint

- **Method:** `POST`
- **Path:** `/incident-cmd/v1/webhook`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [Create Webhook](https://docs.pinghome.io/incident-management/ruleset-management-and-event-handling/create-webhook/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Webhook name. |
| `description` | body | `string` | no | Webhook description. |
