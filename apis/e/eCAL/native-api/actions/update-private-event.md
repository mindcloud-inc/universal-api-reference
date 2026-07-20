# Update Private Event with ECAL

Updates a subscriber's private ECAL event.

## Endpoint

- **Method:** `PUT`
- **Path:** `/event/:eventIdOrReference`
- **Base URL:** `https://api.ecal.com/apiv2`
- **Official documentation:** [Update Private Event](https://docs.ecal.com/reference/private/single.html#put-private-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventIdOrReference` | path | `string` | yes | Private event ID or reference accepted by the update endpoint. |
| `requestBody` | body | `object` | yes | JSON object matching ECAL's private event update payload. |
