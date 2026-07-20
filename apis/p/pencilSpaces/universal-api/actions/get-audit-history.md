# Pencil Spaces: Get Audit History



```
GET https://connect.mindcloud.co/v1/universal/pencilSpaces/latest/actions/get-audit-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pencil Spaces `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pencilSpaces/latest/actions/get-audit-history?connectionId=$CONNECTION_ID&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pencilSpaces/latest/actions/get-audit-history?${params}`, {
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
| `documentId` | string | yes | The audited document to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "change_type": "string",
      "created_at": "string",
      "created_by": {},
      "is_deleted": true,
      "logs": [
        {}
      ],
      "model": "string",
      "model_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `change_type` | string |  |
| `created_at` | string |  |
| `created_by` | object |  |
| `is_deleted` | boolean |  |
| `logs` | array<object> |  |
| `model` | string |  |
| `model_id` | string |  |

## Native endpoint

Through the native Pencil Spaces API, this operation is `GET /audit/:documentId` (base URL `https://apis.pencilapp.com/public/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-audit-history.md) for the provider-specific parameters and requirements.

