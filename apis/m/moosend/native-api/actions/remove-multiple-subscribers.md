# Remove Multiple Subscribers with Moosend

Deletes multiple subscribers from Moosend.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscribers/{{MailingListID}}/remove-many.json`
- **Base URL:** `https://api.moosend.com/v3`
- **Official documentation:** [Remove Multiple Subscribers](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54591-Remove-multiple-subscribers?lang=en_US)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `MailingListID` | path | `string` | yes | The ID of the email list that contains the subscribers you want to remove. |
| `Emails` | body | `object` | yes | A list of subscriber email addresses that you want to remove from the email list. Use a comma (,) to separate the email addresses. |
