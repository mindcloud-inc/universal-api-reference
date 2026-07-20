# Update Subscriber with Maildroppa

Updates a subscriber in Maildroppa without changing the email.

## Endpoint

- **Method:** `PUT`
- **Path:** `/subscribers/{subscriberId}`
- **Base URL:** `https://api.maildroppa.com`
- **Official documentation:** [Update Subscriber](https://api.maildroppa.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `gdprAgreement` | body | `string` | no | Text of GDPR agreement if applicable. |
| `subscriberId` | path | `string` | yes | UUID of the subscriber. |
| `subscriberStatus` | body | `string` | no | Subscriber's status. |
| `tags[]` | body | `array` | no | List of tag identifiers associated with the subscriber. |
| `values[]` | body | `array` | no | List of custom fields for the subscriber. |
