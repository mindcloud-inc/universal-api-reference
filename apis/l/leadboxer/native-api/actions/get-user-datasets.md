# Get User Datasets with Leadboxer

Retrieves datasets for the authenticated user in Leadboxer.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/users/datasets`
- **Base URL:** `https://data.leadboxer.com`
- **Official documentation:** [Get User Datasets](https://developers.leadboxer.com/reference/getuserdatasets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | The user email address. |
