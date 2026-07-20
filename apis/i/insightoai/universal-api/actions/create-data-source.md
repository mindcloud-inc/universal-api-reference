# Insighto.ai: Create Data Source



```
POST https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/create-data-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insighto.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/create-data-source" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dsType": "pdf"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/create-data-source', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dsType": "pdf"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dsType` | list<string> | yes | Datasource type to create. One of: `doc`, `http`, `image`, `pdf`, `text_blob`, `text_image`, `tool`. Example: `pdf`. |
| `name` | string | no | Datasource name. Example: `FAQ Knowledge Base`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "description": "string",
      "ds_status": "string",
      "ds_type": "string",
      "id": "string",
      "name": "Ava Chen",
      "org_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object |  |
| `description` | string |  |
| `ds_status` | string |  |
| `ds_type` | string |  |
| `id` | string |  |
| `name` | string |  |
| `org_id` | string |  |

## Native endpoint

Through the native Insighto.ai API, this operation is `POST /datasource` (base URL `https://api.insighto.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-data-source.md) for the provider-specific parameters and requirements.

