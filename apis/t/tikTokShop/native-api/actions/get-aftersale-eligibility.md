# Get Aftersale Eligibility with TikTok Shop

## Endpoint

- **Method:** `GET`
- **Path:** `/return_refund/202602/orders/:order_id/aftersale_eligibility`
- **Base URL:** `https://open-api.tiktokglobalshop.com/`
- **Official documentation:** [Get Aftersale Eligibility](https://partner.tiktokshop.com/docv2/page/get-aftersale-eligibility-202602)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_id` | path | `string` | yes | — |
| `shop_cipher` | query | `string` | yes | — |
| `initiate_aftersale_user` | query | `list<string>` | no | Accepted values: `BUYER`, `SELLER`. |
| `request_types` | query | `list<string>` | no | Accepted values: `CANCEL`, `REFUND`, `RETURN_AND_REFUND`. Send multiple values as a string separated by `,`. |
