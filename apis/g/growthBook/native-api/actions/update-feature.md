# Partially update a feature with GrowthBook

Updates an existing feature in GrowthBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/features/:id`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Partially update a feature](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The id of the requested resource |
| `description` | body | `string` | no | Description of the feature |
| `archived` | body | `boolean` | no | — |
| `project` | body | `string` | no | An associated project ID |
| `owner` | body | `string` | no | The userId or email address of the owner. If an email address is provided, it will be used to look up the userId of the matching organization member. If an ID is provided, it will be validated as existing in the organization. |
| `defaultValue` | body | `string` | no | — |
| `tags` | body | `list<string>` | no | List of associated tags. Will override tags completely with submitted list |
| `environments` | body | `object` | no | — |
| `prerequisites` | body | `list<string>` | no | Feature IDs. Each feature must evaluate to `true` |
| `jsonSchema` | body | `string` | no | Use JSON schema to validate the payload of a JSON-type feature value (enterprise only). |
| `customFields` | body | `object` | no | — |
| `holdout` | body | `object` | no | — |
