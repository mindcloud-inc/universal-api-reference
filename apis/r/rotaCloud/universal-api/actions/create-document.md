# RotaCloud: Create Document

Creates a document in RotaCloud.

```
POST https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bucket": "string",
  "key": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bucket": "string",
    "key": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bucket` | string | yes | Storage bucket containing the file. |
| `key` | string | yes | Storage key of the file. |
| `name` | string | yes | Document name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_id": 1,
      "bucket": "string",
      "extension": "string",
      "folder_id": 1,
      "id": 1,
      "key": "string",
      "name": "Ava Chen",
      "public": true,
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
| `bucket` | string |  |
| `extension` | string |  |
| `folder_id` | number |  |
| `id` | number |  |
| `key` | string |  |
| `name` | string |  |
| `public` | boolean |  |
| `user` | number |  |
| `users` | array<number> |  |

## Native endpoint

Through the native RotaCloud API, this operation is `POST /v1/documents` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document.md) for the provider-specific parameters and requirements.

