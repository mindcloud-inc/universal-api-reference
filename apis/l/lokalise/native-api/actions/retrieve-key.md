# Retrieve Key with Lokalise

Retrieves a key from a Lokalise project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/keys/:key_id`
- **Base URL:** `https://api.lokalise.com/api2`
- **Official documentation:** [Retrieve Key](https://developers.lokalise.com/reference/retrieve-a-key)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Lokalise project identifier. |
| `key_id` | path | `string` | yes | Lokalise key identifier. |
