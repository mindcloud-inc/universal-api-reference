# Create Subscriber with Maildroppa

Creates a new subscriber in Maildroppa without double opt-in.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscribers`
- **Base URL:** `https://api.maildroppa.com`
- **Official documentation:** [Create Subscriber](https://api.maildroppa.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `gdprAgreement` | body | `string` | no | Text of GDPR agreement if applicable. |
| `subscriberStatus` | body | `string` | no | Subscriber's status. |
| `tags[]` | body | `array` | no | List of tag identifiers associated with the subscriber. |
| `values[]` | body | `array` | no | List of custom fields for the subscriber. |
