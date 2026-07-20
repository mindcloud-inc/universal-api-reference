# List Labels with AnnounceKit

Retrieves labels for a project in AnnounceKit.

## Endpoint

- **Method:** `POST`
- **Path:** `/gq/v2`
- **Base URL:** `https://announcekit.app`
- **Official documentation:** [List Labels](https://announcekit.app/docs/graphql-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `string` | yes | AnnounceKit project id used to retrieve labels. Defaults to the project id provided for this build. |
