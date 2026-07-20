# Get Issue with Sifter

Retrieves a specific issue from Sifter.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/issues/:issue_id`
- **Base URL:** `https://{subdomain}.sifterapp.com/api`
- **Official documentation:** [Get Issue](https://sifterapp.com/developer/documentation/issues/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `issue_id` | path | `number` | yes | The Sifter issue ID. |
| `project_id` | path | `number` | yes | The Sifter project ID. |
