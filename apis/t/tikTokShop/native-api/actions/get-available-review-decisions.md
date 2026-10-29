# Get Available Review Decisions with TikTok Shop

## Endpoint

- **Method:** `GET`
- **Path:** `/return_refund/202606/review_decision`
- **Base URL:** `https://open-api.tiktokglobalshop.com/`
- **Official documentation:** [Get Available Review Decisions](https://partner.tiktokshop.com/docv2/page/get-available-review-decisions-202606)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `return_or_cancel_id` | query | `string` | yes | Use a reverse main order, aftersales request, or return merchandise authorization ID. |
| `seller_id` | query | `string` | yes | Seller/shop identifier; kept as text to preserve the full ID. |
| `shop_cipher` | query | `string` | yes | — |
| `check_decisions` | query | `list<string>` | no | Accepted values: `APPROVE_RECEIVED_PACKAGE`, `APPROVE_REFUND`, `APPROVE_REPLACEMENT`, `APPROVE_REQUEST_CANCEL`, `APPROVE_RETURN`, `DIRECT_REFUND`, `ISSUE_EXCHANGE_REFUND`, `ISSUE_REPLACEMENT_REFUND`, `OFFER_PARTIAL_REFUND`, `OFFER_PARTIAL_REFUND_AFTER_RECEIVING_PKG`, `REJECT_RECEIVED_PACKAGE`, `REJECT_REFUND`, `REJECT_REPLACEMENT`, `REJECT_REQUEST_CANCEL`, `REJECT_RETURN`. Send multiple values as a string separated by `,`. |
| `locale` | query | `string` | no | — |
