# Create Avatar with Colossyan

Creates a new avatar in Colossyan.

## Endpoint

- **Method:** `POST`
- **Path:** `/assets/actors`
- **Base URL:** `https://app.colossyan.com/api/v1`
- **Official documentation:** [Create Avatar](https://docs.colossyan.com/avatar-creation/create-avatar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `displayName` | body | `string` | yes | Name to display for the new avatar. |
| `sourceFileUrl` | body | `string` | yes | Public image or video URL used to generate the avatar. |
| `gender` | body | `string` | yes | Gender label for the new avatar. Accepted values: `0`, `1`. |
