# Create Contact with Go4Clients

Creates a new contact in Go4Clients.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/groupscontacts/contacts/v1.0`
- **Base URL:** `https://cloud.go4clients.com:8580`
- **Official documentation:** [Create Contact](https://apidoc.go4clients.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mobileNumber` | body | `string` | yes | Contact phone number. |
| `name` | body | `string` | no | Custom field value for name. |
| `sex` | body | `string` | no | Custom field value for sex. |
| `weight` | body | `string` | no | Custom field value for weight. |
| `height` | body | `string` | no | Custom field value for height. |
