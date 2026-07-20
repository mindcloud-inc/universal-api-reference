# Get Mailing List Details with Moosend

Retrieves mailing list details from Moosend.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/{{MailingListID}}/details.json`
- **Base URL:** `https://api.moosend.com/v3`
- **Official documentation:** [Get Mailing List Details](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54571-Get-mailing-list-details?lang=en_US)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `MailingListID` | path | `string` | yes | The ID of the email list that contains the details you are requesting. |
| `WithStatistics` | query | `string` | no | Specifies whether to fetch statistics for the subscribers. Possible values: true (Default) and false . |
