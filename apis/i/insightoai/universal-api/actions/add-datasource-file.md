# Insighto.ai: Add Datasourcefile



```
PUT https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/add-datasource-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insighto.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/add-datasource-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "datasourceId": "3c90c3cc-0d44-4b50-8888-8dd25736052a",
  "dsType": "pdf",
  "datasourcefileFile": "https://example.com/file.pdf"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/add-datasource-file', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "datasourceId": "3c90c3cc-0d44-4b50-8888-8dd25736052a",
    "dsType": "pdf",
    "datasourcefileFile": "https://example.com/file.pdf"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `datasourceId` | string | yes | The UUID id of the datasource. Example: `3c90c3cc-0d44-4b50-8888-8dd25736052a`. |
| `dsType` | list<string> | yes | Datasource type for the uploaded file. One of: `doc`, `http`, `image`, `pdf`, `text_blob`, `text_image`, `tool`. Example: `pdf`. |
| `datasourcefileFile` | file | yes | File to upload to the datasource. Example: `https://example.com/file.pdf`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "description": "string",
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
| `ds_type` | string |  |
| `id` | string |  |
| `name` | string |  |
| `org_id` | string |  |

## Native endpoint

Through the native Insighto.ai API, this operation is `POST /datasource/:datasource_id/file` (base URL `https://api.insighto.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-datasource-file.md) for the provider-specific parameters and requirements.

