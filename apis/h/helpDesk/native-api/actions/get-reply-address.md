# Get Reply Address with HelpDesk

Retrieves a reply address from HelpDesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/replyAddresses/:replyAddressID`
- **Base URL:** `https://api.helpdesk.com`
- **Official documentation:** [Get Reply Address](https://api.helpdesk.com/docs#tag/Reply-addresses/operation/replyAddressRead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `replyAddressID` | path | `string` | yes | The HelpDesk reply address ID. |
