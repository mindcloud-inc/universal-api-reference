# Send Referral Emails with Yotpo Loyalty & Referrals

Sends referral emails from Yotpo Loyalty & Referrals.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/referral/share`
- **Base URL:** `https://loyalty.yotpo.com`
- **Official documentation:** [Send Referral Emails](https://loyaltyapi.yotpo.com/reference/send-referral-emails-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address of the referring customer. |
| `customer_id` | body | `string` | no | Customer identifier for the referring customer. |
| `emails` | body | `string` | yes | Comma-separated list of email addresses to share the referral link with. |
