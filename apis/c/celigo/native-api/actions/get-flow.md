# Get Flow with Celigo

## Endpoint

- **Method:** `GET`
- **Path:** `/flows/:flowId`
- **Base URL:** `https://{apiHost}/v1`
- **Official documentation:** [Get Flow](https://developer.celigo.com/api/api-reference/integrations-and-flows/flows)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `flowId` | path | `list<string>` | yes | Flow to get. |
| `mergeInstance` | query | `boolean` | no | For an instance of a multi-instance flow, merge in the abstract flow configuration. |
