# ClustDoc: Create Data Field



```
POST https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/create-data-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClustDoc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/create-data-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "parent_type": "dossier",
  "type": "text"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/create-data-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "parent_type": "dossier",
    "type": "text"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Data field name. |
| `parent_type` | string | yes | Parent resource type for the data field. Default: `dossier`. |
| `type` | string | yes | Data field type, for example text. Default: `text`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "parent_type": "string",
      "rank": 1,
      "slug": "string",
      "team_id": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | number |  |
| `name` | string |  |
| `parent_type` | string |  |
| `rank` | number |  |
| `slug` | string |  |
| `team_id` | number |  |
| `type` | string |  |

## Native endpoint

Through the native ClustDoc API, this operation is `POST /data-fields` (base URL `https://api.clustdoc.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-data-field.md) for the provider-specific parameters and requirements.

