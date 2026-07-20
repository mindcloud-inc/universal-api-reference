# List Subscribers with Moosend

Retrieves subscribers from Moosend by status.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/{{MailingListID}}/subscribers/{{Status}}.json`
- **Base URL:** `https://api.moosend.com/v3`
- **Official documentation:** [List Subscribers](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54575-Get-all-subscribers?lang=en_US)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `MailingListID` | path | `string` | yes | The ID of the email list containing the subscribers. |
| `Status` | path | `string` | yes | Specifies the type of subscriber statistics results to return. Possible values: Subscribed  ,  Unsubscribed  ,  Bounced ,  Removed . |
| `Page` | query | `number` | no | The page of subscriber statistics results to return. |
| `PageSize` | query | `number` | no | The page size of subscriber statistics results to return. |
