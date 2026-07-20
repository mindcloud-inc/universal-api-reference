# Partially update a single saved group with GrowthBook

Updates an existing saved group in GrowthBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/saved-groups/:id`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Partially update a single saved group](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The id of the requested resource |
| `name` | body | `string` | no | The display name of the Saved Group |
| `condition` | body | `string` | no | When type = 'condition', this is the JSON-encoded condition for the group |
| `values` | body | `list<string>` | no | When type = 'list', this is the list of values for the attribute key |
| `owner` | body | `string` | no | The userId or email address of the owner. If an email address is provided, it will be used to look up the userId of the matching organization member. If an ID is provided, it will be validated as existing in the organization. |
| `projects` | body | `list<string>` | no | — |
