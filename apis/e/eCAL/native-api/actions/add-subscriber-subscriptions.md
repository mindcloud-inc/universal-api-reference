# Add Subscriber Subscriptions with ECAL

Adds calendar subscriptions to an ECAL subscriber.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscriber/:ecalId/subscriptions/add`
- **Base URL:** `https://api.ecal.com/apiv2`
- **Official documentation:** [Add Subscriber Subscriptions](https://docs.ecal.com/reference/apiv2/subscriber.html#post-apiv2subscriberidsubscriptionsadd)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ecalId` | path | `string` | yes | Subscriber ecal_id value. |
| `requestBody` | body | `object` | yes | JSON object matching ECAL's add subscriptions body, including calendar identifiers as documented. |
