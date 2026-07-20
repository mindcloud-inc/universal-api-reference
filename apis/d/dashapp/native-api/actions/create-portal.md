# Create Portal with Dash.app

Creates a new portal in Dash.app.

## Endpoint

- **Method:** `POST`
- **Path:** `/portals`
- **Base URL:** `https://api-v2.dash.app`
- **Official documentation:** [Create Portal](https://api-docs.dash.app/dash/openapi/portals/postportal)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assetPermittedActions` | body | `string` | no | Portal asset permission mode |
| `name` | body | `string` | yes | Portal name |
| `showRecentlyAddedAssets` | body | `boolean` | yes | Whether to show recently added assets |
| `slug` | body | `string` | yes | Portal slug |
| `welcomeMessage` | body | `object` | yes | Portal welcome message object |
| `whitelistedFolderFieldOptionIds[]` | body | `array<string>` | yes | Folder field option IDs available in the portal |
