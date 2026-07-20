# Delete Private Event with ECAL

Deletes a subscriber's private ECAL event.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/event/:eventIdOrReference`
- **Base URL:** `https://api.ecal.com/apiv2`
- **Official documentation:** [Delete Private Event](https://docs.ecal.com/reference/private/single.html#delete-private-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventIdOrReference` | path | `string` | yes | Private event ID or reference accepted by the delete endpoint. |
