# Delete Mailing List with Moosend

Deletes an existing mailing list from Moosend.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/lists/{{MailingListID}}/delete.json`
- **Base URL:** `https://api.moosend.com/v3`
- **Official documentation:** [Delete Mailing List](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54569-Delete-a-mailing-list?lang=en_US)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `MailingListID` | path | `string` | yes | The ID of the email list to be deleted. |
