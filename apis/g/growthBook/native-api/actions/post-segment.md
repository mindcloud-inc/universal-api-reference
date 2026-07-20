# Create a single segment with GrowthBook

Creates a new segment in GrowthBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/segments`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Create a single segment](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the segment |
| `owner` | body | `string` | no | The userId or email address of the owner. If an email address is provided, it will be used to look up the userId of the matching organization member. If an ID is provided, it will be validated as existing in the organization. |
| `description` | body | `string` | no | Description of the segment |
| `datasourceId` | body | `string` | yes | ID of the datasource this segment belongs to |
| `identifierType` | body | `string` | yes | Type of identifier (user, anonymous, etc.) |
| `projects` | body | `list<string>` | no | List of project IDs for projects that can access this segment |
| `managedBy` | body | `string` | no | Where this Segment must be managed from. If not set (empty string), it can be managed from anywhere. |
| `type` | body | `string` | yes | GrowthBook supports two types of Segments, SQL and FACT. SQL segments are defined by a SQL query, and FACT segments are defined by a fact table and filters. |
| `query` | body | `string` | no | SQL query that defines the Segment. This is required for SQL segments. |
| `factTableId` | body | `string` | no | ID of the fact table this segment belongs to. This is required for FACT segments. |
| `filters` | body | `list<string>` | no | Optional array of fact table filter ids that can further define the Fact Table based Segment. |
