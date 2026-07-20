# Bulk Add Contacts To Group By Group Name with Growby

Adds multiple contacts to a Growby group by group name.

## Endpoint

- **Method:** `POST`
- **Path:** `/groups/:groupname/contacts/:contactlist`
- **Base URL:** `https://api.growby.net`
- **Official documentation:** [Bulk Add Contacts To Group By Group Name](https://www.postman.com/growby-documentation/growby-api/documentation/i4ul9w0/growby-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupname` | path | `string` | yes | Exact Growby group name. |
| `contactlist` | path | `string` | yes | Comma-separated list of Growby contact ids. |
