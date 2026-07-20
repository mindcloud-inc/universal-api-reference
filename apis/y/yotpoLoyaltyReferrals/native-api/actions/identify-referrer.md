# Identify Referrer with Yotpo Loyalty & Referrals

Finds or creates a referral link in Yotpo Loyalty & Referrals.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/referral/referrer`
- **Base URL:** `https://loyalty.yotpo.com`
- **Official documentation:** [Identify Referrer](https://loyaltyapi.yotpo.com/reference/identify-referrer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address of the referring customer. |
| `first_name` | body | `string` | no | Optional first name for the referring customer. |
| `last_name` | body | `string` | no | Optional last name for the referring customer. |
