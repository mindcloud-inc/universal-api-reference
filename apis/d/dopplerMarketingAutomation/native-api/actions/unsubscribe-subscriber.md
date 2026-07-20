# Unsubscribe Subscriber with Doppler Marketing Automation

Updates a subscriber to unsubscribed in Doppler Marketing Automation.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountName/unsubscribed`
- **Base URL:** `https://restapi.fromdoppler.com`
- **Official documentation:** [Unsubscribe Subscriber](https://restapi.fromdoppler.com/docs/rels/unsubscribe)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Subscriber email address to unsubscribe. |
