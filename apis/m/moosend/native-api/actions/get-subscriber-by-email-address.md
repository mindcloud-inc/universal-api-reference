# Get Subscriber By Email Address with Moosend

Finds a subscriber in Moosend by email address.

## Endpoint

- **Method:** `GET`
- **Path:** `/subscribers/{{MailingListID}}/view.json`
- **Base URL:** `https://api.moosend.com/v3`
- **Official documentation:** [Get Subscriber By Email Address](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54581-Get-subscriber-by-email-address?lang=en_US)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `MailingListID` | path | `string` | yes | The ID of the email list that contains the subscriber. |
| `Email` | query | `string` | yes | The email address of the subscriber. |
