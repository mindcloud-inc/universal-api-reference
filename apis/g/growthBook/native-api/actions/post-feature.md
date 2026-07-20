# Create a single feature with GrowthBook

Creates a new feature in GrowthBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/features`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Create a single feature](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | A unique key name for the feature. Feature keys can only include letters, numbers, hyphens, and underscores. |
| `archived` | body | `boolean` | no | — |
| `description` | body | `string` | no | Description of the feature |
| `owner` | body | `string` | yes | The userId or email address of the owner. If an email address is provided, it will be used to look up the userId of the matching organization member. If an ID is provided, it will be validated as existing in the organization. |
| `project` | body | `string` | no | An associated project ID |
| `valueType` | body | `string` | yes | The data type of the feature payload. Boolean by default. |
| `defaultValue` | body | `string` | yes | Default value when feature is enabled. Type must match `valueType`. |
| `tags` | body | `list<string>` | no | List of associated tags |
| `environments` | body | `object` | no | A dictionary of environments that are enabled for this feature. Keys supply the names of environments. Environments belong to organization and are not specified will be disabled by default. |
| `prerequisites` | body | `list<string>` | no | Feature IDs. Each feature must evaluate to `true` |
| `jsonSchema` | body | `string` | no | Use JSON schema to validate the payload of a JSON-type feature value (enterprise only). |
| `customFields` | body | `object` | no | — |
