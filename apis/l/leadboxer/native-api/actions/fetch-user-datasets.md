# Fetch User Datasets with Leadboxer

Retrieves datasets for a user in Leadboxer.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/user-datasets`
- **Base URL:** `https://data.leadboxer.com`
- **Official documentation:** [Fetch User Datasets](https://developers.leadboxer.com/reference/getuserdatasets_1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | query | `string` | yes | The Leadboxer account ID. |
| `email` | query | `string` | yes | The user email address. |
