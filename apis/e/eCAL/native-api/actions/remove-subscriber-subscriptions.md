# Remove Subscriber Subscriptions with ECAL

Removes calendar subscriptions from an ECAL subscriber.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscriber/:ecalId/subscriptions/remove`
- **Base URL:** `https://api.ecal.com/apiv2`
- **Official documentation:** [Remove Subscriber Subscriptions](https://docs.ecal.com/reference/apiv2/subscriber.html#post-apiv2subscriberidsubscriptionsremove)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ecalId` | path | `string` | yes | Subscriber ecal_id value. |
| `requestBody` | body | `object` | yes | JSON object matching ECAL's remove subscriptions body, including calendar identifiers as documented. |
