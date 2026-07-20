# Pinata: Get File by ID

Retrieves a file from Pinata by ID.

```
GET https://connect.mindcloud.co/v1/universal/pinata/latest/actions/get-file-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinata/latest/actions/get-file-by-id?connectionId=$CONNECTION_ID&id=string&network=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "network": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinata/latest/actions/get-file-by-id?${params}`, {
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
| `id` | string | yes | ID of the target file. |
| `network` | string | yes | Target network (`public` or `private`). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cid": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "expires_at": "2026-05-07T12:00:00.000Z",
      "group_id": "string",
      "id": "string",
      "keyvalues": {},
      "mime_type": "string",
      "name": "Ava Chen",
      "number_of_files": 1,
      "size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cid` | string |  |
| `created_at` | date |  |
| `expires_at` | date |  |
| `group_id` | string |  |
| `id` | string |  |
| `keyvalues` | object |  |
| `mime_type` | string |  |
| `name` | string |  |
| `number_of_files` | number |  |
| `size` | number |  |

## Native endpoint

Through the native Pinata API, this operation is `GET /v3/files/:network/:id` (base URL `https://api.pinata.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file-by-id.md) for the provider-specific parameters and requirements.

