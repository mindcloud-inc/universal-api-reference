# Create Contact with ThriveDesk

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contacts`
- **Base URL:** `https://api.thrivedesk.com`
- **Official documentation:** [Create Contact](https://wordpress.org/plugins/thrivedesk/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Contact name. |
| `email` | body | `string` | yes | Contact email address. Required by ThriveDesk. |
