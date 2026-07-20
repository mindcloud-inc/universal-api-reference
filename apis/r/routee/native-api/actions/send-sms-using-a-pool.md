# Send SMS using a Pool with Routee

Sends SMS using a pool with Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/pools/my/:poolId/sms`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Send SMS using a Pool](https://docs.routee.net/reference/send-sms-using-a-pool)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `poolId` | path | `string` | yes | The tracking id of the pool. |
| `to` | body | `string` | yes | The recipient of the SMS. Format with a '+' and country code e.g., +3069485xxxxx (E.164 format). |
| `poolStrategy` | body | `string` | yes | The strategy to follow when picking a sender from the pool. Values: Numeric, Alphanumeric |
| `body` | body | `string` | yes | The body of the SMS message. |
| `urlShortener` | body | `object` | no | [OPTIONAL] If present, each link that exist in message body will be replaced by a Shortened URL. NOTE: Links are recognized by the prefix "http://" or "https://" and are separated by the next word or character with space. Keep in mind that adding any character like '.' ',' etc, other than space at the end of the link, will be recognized as part of the url and it will result to a shortened url that redirects to a wrong destination. |
