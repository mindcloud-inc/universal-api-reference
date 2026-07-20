# Update Graph with Pixela

Updates an existing graph definition in Pixela.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/users/:username/graphs/:graphID`
- **Base URL:** `https://pixe.la`
- **Official documentation:** [Update Graph](https://docs.pixe.la/entry/put-graph)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | path | `string` | yes | Pixela username in the request path. |
| `graphID` | path | `string` | yes | Pixela graph identifier. |
| `name` | body | `string` | no | Updated graph display name. |
| `unit` | body | `string` | no | Updated unit for recorded quantities. |
| `color` | body | `string` | no | Updated graph color: shibafu, momiji, sora, ichou, ajisai, or kuro. |
| `timezone` | body | `string` | no | TZ database timezone name, such as UTC or Asia/Tokyo. |
| `description` | body | `string` | no | Graph description, up to 256 characters. Maximum length: 256. |
| `startOnMonday` | body | `boolean` | no | Make the calendar heatmap start on Monday. |
| `purgeCacheURLs[]` | body | `array<string>` | no | Advanced list of URLs to purge when the graph is updated. Maximum 5 URLs. |
| `selfSufficient` | body | `string` | no | Supporter-limited SVG self-recording mode: none, increment, or decrement. |
| `isSecret` | body | `boolean` | no | Supporter-limited option to hide this graph from the graph list page. |
| `publishOptionalData` | body | `boolean` | no | Supporter-limited option to include optional pixel data in generated SVG attributes. |
