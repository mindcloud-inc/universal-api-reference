# Get Decision Eligibility with TikTok Shop

## Endpoint

- **Method:** `GET`
- **Path:** `/return_refund/202601/decision_eligibility`
- **Base URL:** `https://open-api.tiktokglobalshop.com/`
- **Official documentation:** [Get Decision Eligibility](https://partner.tiktokshop.com/docv2/page/get-decision-eligibility-202601)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `return_or_cancel_id` | query | `string` | yes | Use a return or cancellation request ID, rather than an order ID. |
| `shop_cipher` | query | `string` | yes | — |
| `check_decisions` | query | `list<string>` | no | Accepted values: `APPROVE_RECEIVED_PACKAGE`, `APPROVE_REFUND`, `APPROVE_REPLACEMENT`, `APPROVE_REQUEST_CANCEL`, `APPROVE_RETURN`, `DIRECT_REFUND`, `ISSUE_EXCHANGE_REFUND`, `ISSUE_REPLACEMENT_REFUND`, `REJECT_RECEIVED_PACKAGE`, `REJECT_REFUND`, `REJECT_REPLACEMENT`, `REJECT_REQUEST_CANCEL`, `REJECT_RETURN`. Send multiple values as a string separated by `,`. |
| `locale` | query | `string` | no | — |
