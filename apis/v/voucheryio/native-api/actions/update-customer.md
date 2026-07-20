# Update Customer with Vouchery.io

## Endpoint

- **Method:** `PUT`
- **Path:** `/customers/:identifier`
- **Base URL:** `https://mindcloud.sandbox.vouchery.app/api/v2.1`
- **Official documentation:** [Update Customer](https://docs.vouchery.io/reference/putapiv21customersidentifier)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `categories` | body | `string` | yes | Customer categories as a JSON array string. |
| `email` | body | `string` | no | Updated customer email. |
| `identifier` | path | `string` | yes | Customer identifier from Vouchery. |
| `loyalty_points` | body | `number` | no | Updated loyalty points total. |
| `metadata` | body | `string` | yes | Customer metadata as a JSON object string. |
| `name` | body | `string` | no | Updated customer name. |
| `referral_code` | body | `string` | no | Updated referral code. |
