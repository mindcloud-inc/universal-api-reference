# Create Contact with Close

Creates a new contact in Close.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact/`
- **Base URL:** `https://api.close.com/api/v1`
- **Official documentation:** [Create Contact](https://developer.close.com/resources/contacts/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lead_id` | body | `string` | yes | Parent lead ID. |
| `name` | body | `string` | no | Contact name. |
| `title` | body | `string` | no | Job title. |
