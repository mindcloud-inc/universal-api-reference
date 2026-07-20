# DataBridge: Batch Ingest Files

Creates documents in DataBridge from multiple files.

```
POST https://connect.mindcloud.co/v1/universal/dataBridge/latest/actions/batch-ingest-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataBridge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dataBridge/latest/actions/batch-ingest-files" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dataBridge/latest/actions/batch-ingest-files', {
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
      "documents": [
        {}
      ],
      "errors": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documents` | array<object> |  |
| `errors` | array<object> |  |

## Native endpoint

Through the native DataBridge API, this operation is `POST /ingest/files` (base URL `https://api.morphik.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-ingest-files.md) for the provider-specific parameters and requirements.

