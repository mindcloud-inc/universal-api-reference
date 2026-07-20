# List Mention Suggestions with Filestage

Retrieves mention suggestions from Filestage.

## Endpoint

- **Method:** `GET`
- **Path:** `/steps/{stepId}/mention-suggestions`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [List Mention Suggestions](https://developers.filestage.io/docs/api/i6yb0mvykt4ru-get-mention-suggestions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `isTeamOnlyComment` | query | `boolean` | no | Should suggest only reviewers and team members with access to the project |
| `stepId` | path | `string` | yes | — |
