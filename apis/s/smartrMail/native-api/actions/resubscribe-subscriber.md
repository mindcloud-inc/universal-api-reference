# Resubscribe Subscriber with SmartrMail

Resubscribes a subscriber in SmartrMail by identifier.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscribers/:email_or_phone_or_uid/resubscribe`
- **Base URL:** `https://go.smartrmail.com/api/v1`
- **Official documentation:** [Resubscribe Subscriber](https://docs.smartrmail.com/en/articles/636619-manage-individual-subscribers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email_or_phone_or_uid` | path | `string` | yes | The subscriber email address, phone number, or UID. |
