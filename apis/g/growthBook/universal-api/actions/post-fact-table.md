# GrowthBook: Create a single fact table

Creates a new fact table in GrowthBook.

```
POST https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-fact-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-fact-table" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "sample",
  "datasource": "sample",
  "userIdTypes": [
    "sample"
  ],
  "sql": "sample"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-fact-table', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "sample",
    "datasource": "sample",
    "userIdTypes": ["sample"],
    "sql": "sample"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Default: `sample`. |
| `description` | string | no | Description of the fact table |
| `owner` | string | no | The userId or email address of the owner. If an email address is provided, it will be used to look up the userId of the matching organization member. If an ID is provided, it will be validated as existing in the organization. |
| `projects` | list<string> | no | List of associated project ids |
| `tags` | list<string> | no | List of associated tags |
| `datasource` | string | yes | The datasource id Default: `sample`. |
| `userIdTypes` | list<string> | yes | List of identifier columns in this table. For example, "id" or "anonymous_id" Default: `["sample"]`. |
| `sql` | string | yes | The SQL query for this fact table Default: `sample`. |
| `eventName` | string | no | The event name used in SQL template variables |
| `managedBy` | string | no | Set this to "api" to disable editing in the GrowthBook UI |

## Response

```json
{
  "success": true,
  "data": [
    {
      "factTable": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `factTable` | object |  |

## Native endpoint

Through the native GrowthBook API, this operation is `POST /fact-tables` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-fact-table.md) for the provider-specific parameters and requirements.

