# Add Dataset with Leadboxer

Creates a new dataset in Leadboxer.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/datasets`
- **Base URL:** `https://data.leadboxer.com`
- **Official documentation:** [Add Dataset](https://developers.leadboxer.com/reference/adddataset)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | The user email address. |
| `humanName` | body | `string` | yes | The display name for the dataset. |
| `timezone` | body | `string` | yes | The dataset timezone. |
| `userIds[]` | body | `array<number>` | no | Optional list of user IDs to associate. |
| `emails[]` | body | `array<string>` | no | Optional list of email addresses to associate. |
| `sendEmail` | body | `boolean` | no | Whether to send invitation emails. |
