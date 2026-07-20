# Approve Or Reject Conversion with InviteReferrals

## Endpoint

- **Method:** `POST`
- **Path:** `/conversion/confirm`
- **Base URL:** `https://www.ref-r.com/api/v1`
- **Official documentation:** [Approve Or Reject Conversion](https://docs.invitereferrals.com/reference/approvereject-conversion)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_id` | body | `string` | yes | Order identifier of the conversion to confirm or reject. |
| `campaign_id` | body | `number` | yes | InviteReferrals campaign identifier. |
| `event` | body | `string` | yes | Conversion event name associated with the order. |
| `status` | body | `number` | yes | Set to approve or reject the conversion based on InviteReferrals docs. |
