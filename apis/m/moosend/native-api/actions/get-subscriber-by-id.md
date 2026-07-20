# Get Subscriber By Id with Moosend

Retrieves a subscriber from Moosend by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/subscribers/{{MailingListID}}/find/{{SubscriberID}}.json`
- **Base URL:** `https://api.moosend.com/v3`
- **Official documentation:** [Get Subscriber By Id](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54580-Get-subscriber-by-ID?lang=en_US)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `MailingListID` | path | `string` | yes | The ID of the email list that contains the subscriber. |
| `SubscriberID` | path | `string` | yes | The ID of the subscriber. |
