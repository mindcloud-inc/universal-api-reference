# Create a single dimension with GrowthBook

Creates a new dimension in GrowthBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/dimensions`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Create a single dimension](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the dimension |
| `description` | body | `string` | no | Description of the dimension |
| `owner` | body | `string` | no | The userId or email address of the owner. If an email address is provided, it will be used to look up the userId of the matching organization member. If an ID is provided, it will be validated as existing in the organization. |
| `datasourceId` | body | `string` | yes | ID of the datasource this dimension belongs to |
| `identifierType` | body | `string` | yes | Type of identifier (user, anonymous, etc.) |
| `query` | body | `string` | yes | SQL query or equivalent for the dimension |
| `managedBy` | body | `string` | no | Where this dimension must be managed from. If not set (empty string), it can be managed from anywhere. |
