# Create Private Event with ECAL

Creates a private event for an ECAL subscriber.

## Endpoint

- **Method:** `POST`
- **Path:** `/event/`
- **Base URL:** `https://api.ecal.com/apiv2`
- **Official documentation:** [Create Private Event](https://docs.ecal.com/reference/private/single.html#post-private-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ecal_id` | query | `string` | yes | Subscriber ecal_id value that receives the private event. |
| `requestBody` | body | `object` | yes | JSON object matching ECAL's private event creation payload. |
