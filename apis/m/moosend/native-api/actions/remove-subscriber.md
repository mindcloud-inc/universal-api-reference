# Remove Subscriber with Moosend

Deletes an existing subscriber from Moosend.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscribers/{{MailingListID}}/remove.json`
- **Base URL:** `https://api.moosend.com/v3`
- **Official documentation:** [Remove Subscriber](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54588-Remove-a-subscriber?lang=en_US)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `MailingListID` | path | `string` | yes | The ID of the email list that contains the subscriber you want to remove. |
| `Email` | body | `string` | yes | The email address of the subscriber. |
