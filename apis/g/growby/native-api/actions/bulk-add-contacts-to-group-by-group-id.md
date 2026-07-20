# Bulk Add Contacts To Group By Group ID with Growby

Adds multiple contacts to a Growby group by group ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/groups/:groupId/contacts/:contactlist`
- **Base URL:** `https://api.growby.net`
- **Official documentation:** [Bulk Add Contacts To Group By Group ID](https://www.postman.com/growby-documentation/growby-api/documentation/i4ul9w0/growby-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `number` | yes | Numeric Growby group id. |
| `contactlist` | path | `string` | yes | Comma-separated list of Growby contact ids. |
