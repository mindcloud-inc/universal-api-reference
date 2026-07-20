# Create Policy with Coast

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/policies`
- **Base URL:** `https://public.coastpay.com`
- **Official documentation:** [Create Policy](https://coastpay.com/integrations/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `allowedPurchaseTimeWindows` | body | `string` | no | — |
| `type` | body | `string` | yes | Policy type |
| `name` | body | `string` | yes | Name of the policy |
| `timezone` | body | `string` | yes | Policy timezone |
| `customSpendControls[]` | body | `array<object>` | yes | — |
| `globalSpendLimits` | body | `object` | no | Policy global spend limit request |
