# Cancel Sub-Account with LinkedCamp

## Endpoint

- **Method:** `POST`
- **Path:** `/users/cancel`
- **Base URL:** `https://api.linkedcamp.com`
- **Official documentation:** [Cancel Sub-Account](https://api.linkedcamp.com/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Sub-account email address. |
| `reason` | body | `string` | yes | Cancellation reason. |
| `description` | body | `string` | yes | Cancellation description. |
