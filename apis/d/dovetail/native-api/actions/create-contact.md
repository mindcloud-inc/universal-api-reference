# Create Contact with Dovetail

Creates a new contact in your Dovetail workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contacts`
- **Base URL:** `https://dovetail.com/api`
- **Official documentation:** [Create Contact](https://developers.dovetail.com/reference/post_v1-contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Contact email. |
| `name` | body | `string` | yes | Contact name. |
