# Remove User Dataset with Leadboxer

Deletes a user-dataset association in Leadboxer.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/user-datasets`
- **Base URL:** `https://data.leadboxer.com`
- **Official documentation:** [Remove User Dataset](https://developers.leadboxer.com/reference/removeuserdataset)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | The user email address. |
| `userId` | body | `number` | yes | The user ID. |
| `datasetId` | body | `string` | yes | The dataset ID. |
