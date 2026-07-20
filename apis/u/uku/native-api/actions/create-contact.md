# Create Contact with Uku

Creates a new contact in Uku.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://app.getuku.com/api/v1.0`
- **Official documentation:** [Create Contact](https://app.getuku.com/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | body | `string` | yes | Uku client ID |
| `email` | body | `string` | yes | Contact email |
| `name` | body | `string` | yes | Contact name |
