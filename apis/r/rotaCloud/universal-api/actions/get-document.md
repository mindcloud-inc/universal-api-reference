# RotaCloud: Get Document



```
GET https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/get-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/get-document?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/get-document?${params}`, {
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
| `id` | number | yes | The document identifier to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_id": 1,
      "acknowledgements": [
        {}
      ],
      "bucket": "string",
      "created_at": 1,
      "expires": "string",
      "extension": "string",
      "folder_id": 1,
      "id": 1,
      "key": "string",
      "name": "Ava Chen",
      "public": true,
      "requires_acknowledgement": true,
      "requires_signing": true,
      "signature": {},
      "size_kb": 1,
      "user": 1,
      "users": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | number |  |
| `acknowledgements` | array<object> |  |
| `bucket` | string |  |
| `created_at` | number |  |
| `expires` | string |  |
| `extension` | string |  |
| `folder_id` | number |  |
| `id` | number |  |
| `key` | string |  |
| `name` | string |  |
| `public` | boolean |  |
| `requires_acknowledgement` | boolean |  |
| `requires_signing` | boolean |  |
| `signature` | object |  |
| `size_kb` | number |  |
| `user` | number |  |
| `users` | array<number> |  |

## Native endpoint

Through the native RotaCloud API, this operation is `GET /v1/documents/:id` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document.md) for the provider-specific parameters and requirements.

