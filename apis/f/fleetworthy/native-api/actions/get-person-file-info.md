# Get Person File Info with Fleetworthy

## Endpoint

- **Method:** `GET`
- **Path:** `/people/file-info`
- **Base URL:** `https://apis.fleetworthy.com/compliance-api/v1`
- **Official documentation:** [Get Person File Info](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=get-people-file-info)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `personId` | query | `string` | yes | The Fleetworthy person UUID. |
| `onlyActiveDocuments` | query | `boolean` | no | Limit file information to active company and regulated documents. |
