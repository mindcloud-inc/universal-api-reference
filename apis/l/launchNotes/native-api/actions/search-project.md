# Search Project with LaunchNotes

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://app.launchnotes.io`
- **Official documentation:** [Search Project](https://developer.launchnotes.com/index.html#query-projectSearch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | body | `string` | yes | Project to search. |
| `searchTerm` | body | `string` | yes | Search term to match inside the project. |
| `limit` | body | `number` | no | Optional maximum number of results. |
