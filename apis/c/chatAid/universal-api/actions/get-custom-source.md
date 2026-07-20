# Chat Aid: Get Custom Source

Retrieves an existing custom source from Chat Aid.

```
GET https://connect.mindcloud.co/v1/universal/chatAid/latest/actions/get-custom-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chat Aid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatAid/latest/actions/get-custom-source?connectionId=$CONNECTION_ID&id=65e1c08202791119fbe1d476" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "65e1c08202791119fbe1d476"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatAid/latest/actions/get-custom-source?${params}`, {
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
| `id` | string | yes | Custom source ID. Example: `65e1c08202791119fbe1d476`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
      "type": "string",
      "wordCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `id` | string |  |
| `name` | string |  |
| `status` | string |  |
| `type` | string |  |
| `wordCount` | number |  |

## Native endpoint

Through the native Chat Aid API, this operation is `GET /external/sources/custom/:id` (base URL `https://api.chataid.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-custom-source.md) for the provider-specific parameters and requirements.

