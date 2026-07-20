# DataBridge: Query Document

Runs a one-off document analysis in DataBridge.

```
GET https://connect.mindcloud.co/v1/universal/dataBridge/latest/actions/query-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataBridge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataBridge/latest/actions/query-document?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataBridge/latest/actions/query-document?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "combinedMetadata": {},
      "extractedMetadata": {},
      "ingestionDocument": {},
      "ingestionEnqueued": true,
      "ingestionOptions": {},
      "inputMetadata": {},
      "structuredOutput": {},
      "textOutput": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `combinedMetadata` | object |  |
| `extractedMetadata` | object |  |
| `ingestionDocument` | object |  |
| `ingestionEnqueued` | boolean |  |
| `ingestionOptions` | object |  |
| `inputMetadata` | object |  |
| `structuredOutput` | object |  |
| `textOutput` | object |  |

## Native endpoint

Through the native DataBridge API, this operation is `POST /ingest/document/query` (base URL `https://api.morphik.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-document.md) for the provider-specific parameters and requirements.

