# Add Contact To Group By Group ID with Growby

Adds a contact to a Growby group by group ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/groups/:groupId/contacts/:contactId`
- **Base URL:** `https://api.growby.net`
- **Official documentation:** [Add Contact To Group By Group ID](https://www.postman.com/growby-documentation/growby-api/documentation/i4ul9w0/growby-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `number` | yes | Numeric Growby group id. |
| `contactId` | path | `number` | yes | Numeric Growby contact id to add to the group. |
