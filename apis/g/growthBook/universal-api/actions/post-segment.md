# GrowthBook: Create a single segment

Creates a new segment in GrowthBook.

```
POST https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-segment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "sample",
  "datasourceId": "sample_id_1",
  "identifierType": "sample",
  "type": "sample"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-segment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "sample",
    "datasourceId": "sample_id_1",
    "identifierType": "sample",
    "type": "sample"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the segment Default: `sample`. |
| `owner` | string | no | The userId or email address of the owner. If an email address is provided, it will be used to look up the userId of the matching organization member. If an ID is provided, it will be validated as existing in the organization. |
| `description` | string | no | Description of the segment |
| `datasourceId` | string | yes | ID of the datasource this segment belongs to Default: `sample_id_1`. |
| `identifierType` | string | yes | Type of identifier (user, anonymous, etc.) Default: `sample`. |
| `projects` | list<string> | no | List of project IDs for projects that can access this segment |
| `managedBy` | string | no | Where this Segment must be managed from. If not set (empty string), it can be managed from anywhere. |
| `type` | string | yes | GrowthBook supports two types of Segments, SQL and FACT. SQL segments are defined by a SQL query, and FACT segments are defined by a fact table and filters. Default: `sample`. |
| `query` | string | no | SQL query that defines the Segment. This is required for SQL segments. |
| `factTableId` | string | no | ID of the fact table this segment belongs to. This is required for FACT segments. |
| `filters` | list<string> | no | Optional array of fact table filter ids that can further define the Fact Table based Segment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "segment": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `segment` | object |  |

## Native endpoint

Through the native GrowthBook API, this operation is `POST /segments` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-segment.md) for the provider-specific parameters and requirements.

