# Add User Dataset with Leadboxer

Creates a user-dataset association in Leadboxer.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/user-datasets`
- **Base URL:** `https://data.leadboxer.com`
- **Official documentation:** [Add User Dataset](https://developers.leadboxer.com/reference/adduserdataset)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | The user email address. |
| `userId` | body | `number` | yes | The user ID. |
| `datasetId` | body | `string` | yes | The dataset ID. |
| `timezone` | body | `string` | yes | The timezone. |
| `sendEmail` | body | `boolean` | no | Whether to send an email. |
