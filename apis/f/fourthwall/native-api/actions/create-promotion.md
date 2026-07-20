# Create Promotion with Fourthwall

Creates a new promotion in Fourthwall.

## Endpoint

- **Method:** `POST`
- **Path:** `/open-api/v1.0/promotions`
- **Base URL:** `https://api.fourthwall.com`
- **Official documentation:** [Create Promotion](https://docs.fourthwall.com/api-reference/platform/promotions/create-promotion)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `list` | yes | Promotion type. Supported values: SHOP_SINGLE, SHOP_MULTI, MEMBERSHIPS_SINGLE, MEMBERSHIPS_MULTI. Accepted values: `MEMBERSHIPS_MULTI`, `MEMBERSHIPS_SINGLE`, `SHOP_MULTI`, `SHOP_SINGLE`. |
| `code` | body | `string` | no | Promotion code for single-code variants. |
| `codes[]` | body | `array<string>` | no | Array of promotion codes for multi-code variants. |
| `discount` | body | `object` | yes | Discount object. For shop promotions use either a fixed amount discount or percentage discount. For membership promotions use percentage discount. |
| `requirements` | body | `object` | no | Requirements object. For memberships, set newMembersOnly. For shop promotions, minimumOrderValue may be provided. |
| `subscriptionType` | body | `list` | no | Membership subscription type selector for membership promotion variants. Accepted values: `ALL`, `ANNUAL`, `MONTHLY`. |
| `tiers` | body | `object` | no | Membership tiers selector object for membership promotion variants. |
| `appliesToProducts` | body | `object` | no | Selected products object for shop promotion variants. productIds is required if this object is provided. |
| `limits` | body | `object` | no | Promotion limits object for shop promotion variants. oneUsePerCustomer is required if this object is provided. |
