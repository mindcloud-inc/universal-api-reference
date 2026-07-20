# YepCode: Get storage object helper

Retrieves a storage object from YepCode.

```
GET https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/get-storage-object-helper
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YepCode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/get-storage-object-helper?connectionId=$CONNECTION_ID&filename=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filename": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/get-storage-object-helper?${params}`, {
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
| `filename` | string | yes | Storage object filename. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Binary file content returned by the endpoint |

## Native endpoint

Through the native YepCode API, this operation is `GET /storage/objects/:filename` (base URL `https://cloud.yepcode.io/api/{{credentials.team}}/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-storage-object-helper.md) for the provider-specific parameters and requirements.

