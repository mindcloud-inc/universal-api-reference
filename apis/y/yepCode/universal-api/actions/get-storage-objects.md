# YepCode: Get storage objects

Retrieves storage object records from YepCode.

```
GET https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/get-storage-objects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YepCode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/get-storage-objects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/get-storage-objects?${params}`, {
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
| `prefix` | string | no | Filter results to include only objects whose names begin with this prefix. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "link": "https://example.com",
      "md5Hash": "string",
      "name": "Ava Chen",
      "size": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | string | MIME content type of the object |
| `createdAt` | date | Timestamp when the object was created |
| `link` | string | Provider link to the stored object |
| `md5Hash` | string | MD5 hash of the stored object |
| `name` | string | Object filename in storage |
| `size` | number | Object size in bytes |
| `updatedAt` | date | Timestamp when the object was last updated |

## Native endpoint

Through the native YepCode API, this operation is `GET /storage/objects` (base URL `https://cloud.yepcode.io/api/{{credentials.team}}/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-storage-objects.md) for the provider-specific parameters and requirements.

