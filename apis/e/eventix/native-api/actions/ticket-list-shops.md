# Get all Shops this Ticket Type is attached to with Eventix

Retrieves shops for an Eventix ticket type.

## Endpoint

- **Method:** `GET`
- **Path:** `/3.0.0/ticket/:guid/shops`
- **Base URL:** `https://api.weeztix.com`
- **Official documentation:** [Get all Shops this Ticket Type is attached to](https://docs.weeztix.com/api/dashboard/ticket-list-shops)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `guid` | path | `string` | yes | The guid of the Ticket Type. |
