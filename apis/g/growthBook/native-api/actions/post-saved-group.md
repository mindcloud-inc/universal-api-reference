# Create a single saved group with GrowthBook

Creates a new saved group in GrowthBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/saved-groups`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Create a single saved group](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The display name of the Saved Group |
| `type` | body | `string` | no | The type of Saved Group (inferred from other arguments if missing) |
| `condition` | body | `string` | no | When type = 'condition', this is the JSON-encoded condition for the group |
| `attributeKey` | body | `string` | no | When type = 'list', this is the attribute key the group is based on |
| `values` | body | `list<string>` | no | When type = 'list', this is the list of values for the attribute key |
| `owner` | body | `string` | no | The userId or email address of the owner. If an email address is provided, it will be used to look up the userId of the matching organization member. If an ID is provided, it will be validated as existing in the organization. |
| `projects` | body | `list<string>` | no | — |
