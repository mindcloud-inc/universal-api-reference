# List Segments with Moosend

Retrieves segments from Moosend.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/{{MailingListID}}/segments.json`
- **Base URL:** `https://api.moosend.com/v3`
- **Official documentation:** [List Segments](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54611-Get-all-segments?lang=en_US)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `MailingListID` | path | `string` | yes | The ID of the email list that contains the segments. |
