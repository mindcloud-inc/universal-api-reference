# Request Organization with Pledge

Requests an organization in Pledge.

## Endpoint

- **Method:** `POST`
- **Path:** `/organizations`
- **Base URL:** `https://api.pledge.to/v1`
- **Official documentation:** [Request Organization](https://developer.pledge.to/api/#tag/Organizations/operation/requestOrganization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ngo_id` | body | `string` | yes | Employer identification number for the organization request. |
| `contact.email` | body | `string` | yes | Email for the requester contact. |
| `contact.first_name` | body | `string` | yes | First name for the requester contact. |
| `contact.last_name` | body | `string` | yes | Last name for the requester contact. |
| `email` | body | `string` | yes | Email for the requester. |
| `first_name` | body | `string` | yes | First name for the requester. |
| `last_name` | body | `string` | yes | Last name for the requester. |
