# RightSignature: List Documents

Retrieves available documents from your RightSignature account.

```
GET https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/list-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RightSignature `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/list-documents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/list-documents?${params}`, {
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
| `search` | string | no | A search token. |
| `templateId` | string | no | Documents from a specific template |
| `state` | string | no | The document state filter. Must be one of valid document states or comma seperated list of states. Valid document states are: draft, pending, executed, voided, expired, declined, editing |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documents": [
        "string"
      ],
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documents` | array<string> |  |
| `meta` | object |  |

## Native endpoint

Through the native RightSignature API, this operation is `GET /documents` (base URL `https://api.rightsignature.com/public/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-documents.md) for the provider-specific parameters and requirements.

