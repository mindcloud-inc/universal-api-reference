# Add Collaborators to Project with Filestage

Adds collaborators to a Filestage project.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/{projectId}/collaborators`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [Add Collaborators to Project](https://developers.filestage.io/docs/api/xi8qqsa786l43-add-collaborators-to-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Project Id |
| `emails[]` | body | `array<string>` | yes | — |
| `message` | body | `string` | no | — |
| `notifyEmail` | body | `boolean` | no | — |
