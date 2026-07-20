# Get License with HelpDesk

Retrieves a license from HelpDesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/licenses/:licenseID`
- **Base URL:** `https://api.helpdesk.com`
- **Official documentation:** [Get License](https://api.helpdesk.com/docs#tag/Licenses/operation/licensesRead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `licenseID` | path | `string` | yes | Unique HelpDesk license ID. |
