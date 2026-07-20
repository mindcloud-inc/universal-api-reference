# Unsubscribe Subscriber with ECAL

Unsubscribes a subscriber from ECAL.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscriber/:ecalId/unsubscribe`
- **Base URL:** `https://api.ecal.com/apiv2`
- **Official documentation:** [Unsubscribe Subscriber](https://docs.ecal.com/reference/apiv2/subscriber.html#post-apiv2subscriberidunsubscribe)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ecalId` | path | `string` | yes | Subscriber ecal_id value. |
