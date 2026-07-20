# LangChain: List Examples



```
GET https://connect.mindcloud.co/v1/universal/langChain/latest/actions/list-examples
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LangChain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/langChain/latest/actions/list-examples?connectionId=$CONNECTION_ID&datasetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "datasetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/langChain/latest/actions/list-examples?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `datasetId` | string | yes | Dataset identifier required for listing examples. |

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
| `attachment_urls` | object | Optional attachment URLs. |
| `created_at` | date | Creation timestamp. |
| `dataset_id` | string | Dataset UUID containing this example. |
| `id` | string | Example UUID. |
| `inputs` | object | Example input payload. |
| `metadata` | object | Example metadata. |
| `modified_at` | date | Last update timestamp. |
| `name` | string | Example display name. |
| `outputs` | object | Example output payload. |
| `source_run_id` | string | Optional source run UUID. |

## Native endpoint

Through the native LangChain API, this operation is `GET /api/v1/examples` (base URL `https://api.smith.langchain.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-examples.md) for the provider-specific parameters and requirements.

