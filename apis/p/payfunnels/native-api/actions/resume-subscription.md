# Resume Subscription with Payfunnels

Updates a subscription by resuming it in Payfunnels.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/subscriptions/resume`
- **Base URL:** `https://api.payfunnels.com`
- **Official documentation:** [Resume Subscription](https://api.payfunnels.com/api/docs/#resume-subscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | ID of the subscription to resume. |
