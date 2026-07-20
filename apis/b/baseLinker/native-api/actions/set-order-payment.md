# Set Order Payment with BaseLinker

Updates order payment details in BaseLinker.

## Endpoint

- **Method:** `POST`
- **Path:** `/connector.php`
- **Base URL:** `https://api.baselinker.com`
- **Official documentation:** [Set Order Payment](https://api.baselinker.com/index.php?method=setOrderPayment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `order_id` | body | `number` | yes |
| `payment_done` | body | `number` | yes |
| `payment_date` | body | `number` | no |
| `payment_comment` | body | `string` | no |
| `external_payment_id` | body | `string` | no |
