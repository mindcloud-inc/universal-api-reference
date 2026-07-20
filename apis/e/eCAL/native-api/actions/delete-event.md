# Delete Event with ECAL

Deletes an ECAL event by ID or reference.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/event/:eventIdOrReference`
- **Base URL:** `https://api.ecal.com/apiv2`
- **Official documentation:** [Delete Event](https://docs.ecal.com/reference/apiv2/event.html#delete-apiv2eventid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventIdOrReference` | path | `string` | yes | ECAL event ID or reference accepted by the delete endpoint. |
