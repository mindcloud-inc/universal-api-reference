# LangChain: Create Example



```
POST https://connect.mindcloud.co/v1/universal/langChain/latest/actions/create-example
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LangChain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/langChain/latest/actions/create-example" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/langChain/latest/actions/create-example', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "attachment_urls": {},
      "created_at": "2026-05-07T12:00:00.000Z",
      "dataset_id": "string",
      "id": "string",
      "inputs": {},
      "metadata": {},
      "modified_at": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "outputs": {},
      "source_run_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachment_urls` | object | Optional attachment URL map. |
| `created_at` | date | Creation timestamp. |
| `dataset_id` | string | Dataset UUID containing this example. |
| `id` | string | Example UUID. |
| `inputs` | object | Input payload for this example. |
| `metadata` | object | Provider metadata for this example. |
| `modified_at` | date | Last update timestamp. |
| `name` | string | Example display name. |
| `outputs` | object | Output payload for this example. |
| `source_run_id` | string | Optional source run UUID. |

## Native endpoint

Through the native LangChain API, this operation is `POST /api/v1/examples` (base URL `https://api.smith.langchain.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-example.md) for the provider-specific parameters and requirements.

