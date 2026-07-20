# GrowthBook: Update a single fact table

Updates an existing fact table in GrowthBook.

```
PUT https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/update-fact-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/update-fact-table" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "prj_19g6smo332up7"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/update-fact-table', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "prj_19g6smo332up7"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The id of the requested resource Default: `prj_19g6smo332up7`. |
| `name` | string | no |  |
| `description` | string | no | Description of the fact table |
| `owner` | string | no | The userId or email address of the owner. If an email address is provided, it will be used to look up the userId of the matching organization member. If an ID is provided, it will be validated as existing in the organization. |
| `projects` | list<string> | no | List of associated project ids |
| `tags` | list<string> | no | List of associated tags |
| `userIdTypes` | list<string> | no | List of identifier columns in this table. For example, "id" or "anonymous_id" |
| `sql` | string | no | The SQL query for this fact table |
| `eventName` | string | no | The event name used in SQL template variables |
| `columns[]` | array<object> | no | Optional array of columns that you want to update. Only allows updating properties of existing columns. Cannot create new columns or delete existing ones. Columns cannot be added or deleted; column structure is determined by SQL parsing. Slice-related properties require an enterprise license. |
| `columns[]` | array<object> | no | Optional array of columns that you want to update. Only allows updating properties of existing columns. Cannot create new columns or delete existing ones. Columns cannot be added or deleted; column structure is determined by SQL parsing. Slice-related properties require an enterprise license. |
| `columnsError` | string | no |  |
| `managedBy` | string | no | Set this to "api" to disable editing in the GrowthBook UI |
| `archived` | boolean | no |  |

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

Through the native GrowthBook API, this operation is `POST /fact-tables/:id` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-fact-table.md) for the provider-specific parameters and requirements.

