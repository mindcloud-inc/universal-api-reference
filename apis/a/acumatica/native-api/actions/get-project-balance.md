# Get Project Balance with Acumatica

## Endpoint

- **Method:** `GET`
- **Path:** `/:projectId/:projectAction`
- **Base URL:** `{uRL}`
- **Official documentation:** [Get Project Balance](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The ID of a project to retrieve. Provided when you list Projects. Use the links.self property. Example: /entity/Default/23.200.001/Project/e7d81cfc-f596-ef11-8361-0646c1159ab3 |
| `projectAction` | path | `string` | no | Choose from the list or enter an action path to match the schema definition for this entity. |
