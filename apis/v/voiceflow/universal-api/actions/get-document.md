# Voiceflow: Get Document

Retrieves a knowledge base document from Voiceflow.

```
GET https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/get-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voiceflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/get-document?connectionId=$CONNECTION_ID&documentId=69c579d68f9846b75ad7ceed" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "69c579d68f9846b75ad7ceed"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/get-document?${params}`, {
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
| `documentId` | string | yes | ID of the document to fetch. Example: `69c579d68f9846b75ad7ceed`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chunks": [
        {}
      ],
      "data": {},
      "metadata": [
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
| `chunks` | array<object> | Indexed chunks for the document. |
| `data` | object | Document detail payload. |
| `metadata` | array<object> | Additional document metadata rows. |

## Native endpoint

Through the native Voiceflow API, this operation is `GET https://realtime-api.voiceflow.com/v1alpha1/public/knowledge-base/document/:documentId` (base URL `https://general-runtime.voiceflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document.md) for the provider-specific parameters and requirements.

