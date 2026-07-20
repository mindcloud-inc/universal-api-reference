# Update Subscription with Signaturit

Updates an existing subscription in Signaturit.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/subscriptions/:id.json`
- **Base URL:** `https://api.sandbox.signaturit.com/v3`
- **API:** rest
- **Official documentation:** [Update Subscription](https://docs.signaturit.com/api/latest#subscriptions_patch_subscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Identifier of the subscription to update. |
| `url` | body | `string` | yes | Destination URL that will receive Signaturit event payloads. |
| `events` | body | `string` | no | Optional replacement event code or * wildcard. The docs say update accepts the same parameters as create. |
