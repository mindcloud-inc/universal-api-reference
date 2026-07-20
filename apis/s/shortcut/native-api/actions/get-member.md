# Get Member with Shortcut

## Endpoint

- **Method:** `GET`
- **Path:** `/members/:memberPublicId`
- **Base URL:** `https://api.app.shortcut.com/api/v3`
- **Official documentation:** [Get Member](https://developer.shortcut.com/api/rest/v3#Get-Member)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `memberPublicId` | path | `string` | yes | The public ID of the member. |
| `org-public-id` | query | `string` | no | Limit the member lookup to a specific organization. |
