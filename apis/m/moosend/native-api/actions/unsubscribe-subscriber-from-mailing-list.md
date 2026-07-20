# Unsubscribe Subscriber From Mailing List with Moosend

Unsubscribes a subscriber from a Moosend mailing list.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscribers/{{MailingListID}}/unsubscribe.json`
- **Base URL:** `https://api.moosend.com/v3`
- **Official documentation:** [Unsubscribe Subscriber From Mailing List](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54577-Unsubscribe-a-subscriber-from-a-mailing-list?lang=en_US)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `MailingListID` | path | `string` | yes | The ID of the email list from which you want to unsubscribe a subscriber. |
| `Email` | body | `string` | yes | The email address of the subscriber. |
