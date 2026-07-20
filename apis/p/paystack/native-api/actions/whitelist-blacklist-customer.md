# Whitelist/Blacklist Customer with Paystack

## Endpoint

- **Method:** `POST`
- **Path:** `/customer/set_risk_action`
- **Base URL:** `https://api.paystack.co`
- **Official documentation:** [Whitelist/Blacklist Customer](https://paystack.com/docs/api/customer/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customer` | body | `string` | yes |
| `risk_action` | body | `string` | yes |
