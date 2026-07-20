# Create Double Opt-In Subscriber with Maildroppa

Starts double opt-in for a new Maildroppa subscriber.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscribers/opt-in`
- **Base URL:** `https://api.maildroppa.com`
- **Official documentation:** [Create Double Opt-In Subscriber](https://api.maildroppa.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `gdprAgreement` | body | `string` | no | Text of GDPR agreement if applicable. |
| `subscriberStatus` | body | `string` | no | Subscriber's status. |
| `tags` | body | `string` | no | List of tag identifiers associated with the subscriber. |
| `values` | body | `string` | no | List of custom fields for the subscriber. |
