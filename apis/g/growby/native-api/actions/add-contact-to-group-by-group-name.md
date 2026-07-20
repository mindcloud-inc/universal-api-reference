# Add Contact To Group By Group Name with Growby

Adds a contact to a Growby group by group name.

## Endpoint

- **Method:** `POST`
- **Path:** `/groups/:groupname/contacts/:contactId`
- **Base URL:** `https://api.growby.net`
- **Official documentation:** [Add Contact To Group By Group Name](https://www.postman.com/growby-documentation/growby-api/documentation/i4ul9w0/growby-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupname` | path | `string` | yes | Exact Growby group name. |
| `contactId` | path | `number` | yes | Numeric Growby contact id to add to the group. |
