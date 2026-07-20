# Create Add-On with Billwerkplus

Creates an add-on in Billwerkplus.

## Endpoint

- **Method:** `POST`
- **Path:** `/add_on`
- **Base URL:** `https://api.frisbii.com/v1`
- **Official documentation:** [Create Add-On](https://docs.frisbii.com/reference/createaddon)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `handle` | body | `string` | yes | Per account unique handle for the add-on. |
| `name` | body | `string` | yes | Name of add-on. Used as order line text. |
| `amount` | body | `number` | yes | Add-on amount. |
| `type` | body | `list` | yes | Add-on type: on_off or quantity. Accepted values: `0`, `1`. |
| `all_plans` | body | `boolean` | no | Whether all plans are eligible for this add-on. |
| `amount_incl_vat` | body | `boolean` | no | Whether the amount already includes VAT. |
| `description` | body | `string` | no | Optional description of add-on. |
| `currency` | body | `string` | no | Optional ISO 4217 currency code for the add-on. |
| `vat` | body | `number` | no | Optional VAT rate for the add-on. |
| `tax_policy` | body | `string` | no | Optional tax policy handle for the add-on. |
| `eligible_plans[]` | body | `array<string>` | no | Plan handles eligible for this add-on when all plans is false. |
| `entitlements[]` | body | `array<string>` | no | Entitlement handles for the add-on. |
