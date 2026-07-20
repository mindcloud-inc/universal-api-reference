# Get Subscriber with SmartrMail

Retrieves a subscriber from SmartrMail by identifier.

## Endpoint

- **Method:** `GET`
- **Path:** `/subscribers/:email_or_phone_or_uid`
- **Base URL:** `https://go.smartrmail.com/api/v1`
- **Official documentation:** [Get Subscriber](https://docs.smartrmail.com/en/articles/636619-manage-individual-subscribers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email_or_phone_or_uid` | path | `string` | yes | The subscriber email address, phone number, or UID. |
