# PBX Yeastar: Query Phonebook

Retrieves a phonebook from PBX Yeastar.

```
GET https://connect.mindcloud.co/v1/universal/pBXYeastar/latest/actions/query-phonebook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PBX Yeastar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pBXYeastar/latest/actions/query-phonebook?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pBXYeastar/latest/actions/query-phonebook?${params}`, {
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
| `id` | number | yes | Unique phonebook ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "errcode": 1,
      "errmsg": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Phonebook details. |
| `errcode` | number | Yeastar result code. 0 means success. |
| `errmsg` | string | Yeastar result message. |

## Native endpoint

Through the native PBX Yeastar API, this operation is `GET /phonebook/get` (base URL `{{credentials.baseUrl}}/openapi/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-phonebook.md) for the provider-specific parameters and requirements.

