# Update Lead with LinkedCamp

## Endpoint

- **Method:** `POST`
- **Path:** `/leads/update`
- **Base URL:** `https://api.linkedcamp.com`
- **Official documentation:** [Update Lead](https://api.linkedcamp.com/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profileLink` | body | `string` | yes | Lead LinkedIn profile URL. |
| `firstName` | body | `string` | no | Lead first name. |
| `lastName` | body | `string` | no | Lead last name. |
| `email` | body | `string` | no | Lead email address. |
| `emailStatus` | body | `string` | no | Lead email status. |
