# Add Conversion with InviteReferrals

## Endpoint

- **Method:** `POST`
- **Path:** `/conversion/add`
- **Base URL:** `https://www.ref-r.com/api/v1`
- **Official documentation:** [Add Conversion](https://docs.invitereferrals.com/reference/add-conversion)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_id` | body | `string` | yes | Unique order identifier for the conversion. |
| `campaign_id` | body | `number` | yes | InviteReferrals campaign identifier. |
| `referee_name` | body | `string` | yes | Name of the referred customer tied to the conversion. |
| `referee_email` | body | `string` | yes | Email address of the referred customer tied to the conversion. |
| `referrer_code` | body | `string` | no | Referral code given by the referrer to the customer to attribute the conversion. |
| `unique_code` | body | `string` | no | Unique code sent by the referrer to the customer to attribute the conversion. |
