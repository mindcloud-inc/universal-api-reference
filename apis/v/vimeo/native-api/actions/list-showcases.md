# List Showcases with Vimeo

Retrieves a user's showcases from Vimeo.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:user_id/albums`
- **Base URL:** `https://api.vimeo.com`
- **Official documentation:** [List Showcases](https://developer.vimeo.com/api/reference/showcases#get_showcases)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `number` | yes | The ID of the user. |
| `query` | query | `string` | no | The search query to use to filter the results. |
| `sort` | query | `list<string>` | no | The way to sort the results. Accepted values: `alphabetical`, `date`, `duration`, `last_modified`, `videos`. |
| `direction` | query | `list<string>` | no | The sort direction of the results. Accepted values: `asc`, `desc`. |
| `filter_privacy` | query | `list<string>` | no | A comma-separated list of showcase privacies to include. Accepted values: `anybody`, `embed_only`, `nobody`, `password`, `team`, `unlisted`. Send multiple values as a string separated by `,`. |
