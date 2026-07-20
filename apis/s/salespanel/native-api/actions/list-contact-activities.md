# List Contact Activities with Salespanel

Retrieves activities for a contact in Salespanel by ID or email.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/:contact_id/activities/`
- **Base URL:** `https://salespanel.io/api/v1`
- **Official documentation:** [List Contact Activities](https://salespanel.io/docs/#retrieve-activities-of-a-contact)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `string` | yes | The unique ID of the contact whose activities you want to retrieve. |
