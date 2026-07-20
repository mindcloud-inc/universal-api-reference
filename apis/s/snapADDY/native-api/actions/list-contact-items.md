# List Contact Items with snapADDY

## Endpoint

- **Method:** `GET`
- **Path:** `/grabber/v1/contactlist/:listId/contactitems`
- **Base URL:** `https://api.snapaddy.com`
- **Official documentation:** [List Contact Items](https://developers.snapaddy.com/dataquality-rest-api/reference/contact-items-from-contact-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `string` | yes | Contact list identifier |
| `page` | query | `number` | no | Page number |
| `limit` | query | `number` | no | Maximum number of items to return |
