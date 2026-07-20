# List Nodes with LaunchNotes

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://app.launchnotes.io`
- **Official documentation:** [List Nodes](https://developer.launchnotes.com/index.html#query-nodes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | body | `array<string>` | yes | List of node identifiers. |
