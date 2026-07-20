# Update Policy By ID with Coast

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/policies/:policyId`
- **Base URL:** `https://public.coastpay.com`
- **Official documentation:** [Update Policy By ID](https://coastpay.com/integrations/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `policyId` | path | `string` | yes | Coast policy ID of the policy to update. |
| `type` | body | `string` | yes | Updated type for the policy. |
| `name` | body | `string` | yes | Updated name for the policy. |
| `archived` | body | `boolean` | yes | Whether the policy should be archived. |
| `timezone` | body | `string` | yes | Updated timezone for the policy. |
| `customSpendControls[]` | body | `array<object>` | yes | Updated custom spend controls for the policy. |
| `allowedPurchaseTimeWindows` | body | `string` | no | Updated allowed purchase time windows for the policy. |
| `globalSpendLimits` | body | `object` | no | Updated global spend limits for the policy. |
