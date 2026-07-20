# Update Event with ECAL

Updates an ECAL event by ID or reference.

## Endpoint

- **Method:** `PUT`
- **Path:** `/event/:eventIdOrReference`
- **Base URL:** `https://api.ecal.com/apiv2`
- **Official documentation:** [Update Event](https://docs.ecal.com/reference/apiv2/event.html#put-apiv2eventid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventIdOrReference` | path | `string` | yes | ECAL event ID or reference accepted by the update endpoint. |
| `requestBody` | body | `object` | yes | JSON object matching ECAL's update event payload. |
