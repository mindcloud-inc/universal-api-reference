# Get Canned Response with HelpDesk

Retrieves a canned response from HelpDesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/cannedResponses/:cannedResponseID`
- **Base URL:** `https://api.helpdesk.com`
- **Official documentation:** [Get Canned Response](https://api.helpdesk.com/docs#tag/Canned-responses/operation/cannedResponsesRead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cannedResponseID` | path | `string` | yes | The HelpDesk canned response ID. |
