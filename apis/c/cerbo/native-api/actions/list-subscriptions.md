# List Subscriptions with Cerbo

Retrieves subscription records from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/patients/subscriptions`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Subscriptions](https://docs.cer.bo/#tag/Patient-Subscriptions/operation/listPatientSubscriptions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_deleted` | query | `boolean` | no | Returns deleted and current subscriptions if set to true. Default is false. |
| `schedule_frequency` | query | `string` | no | If set to monthly/weekly/annually, it will only return subscriptions billing at that frequency. |
| `subscription_charge_id` | query | `string` | no | ID of a specific charge associated with a subscription-type. If set, it will only return that type of subscription. |
| `charge_owner_user_id` | query | `string` | no | ID of a Cerbo user that gets 'credit' for that subscription. If set, it will only return 'their' subscriptions. |
