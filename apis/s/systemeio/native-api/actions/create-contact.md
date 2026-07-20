# Create Contact with Systeme.io

Creates a new contact in Systeme.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/contacts`
- **Base URL:** `https://api.systeme.io`
- **Official documentation:** [Create Contact](https://developer.systeme.io/reference/post_contact-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Contact email address. |
| `fields[].slug` | body | `string` | no | Custom field slug. |
| `fields[].value` | body | `string` | no | Custom field value. |
| `locale` | body | `string` | no | Contact locale code. |
