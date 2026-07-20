# Fish Audio: Get User Package

Retrieves current user package details from Fish Audio.

```
GET https://connect.mindcloud.co/v1/universal/fishAudio/latest/actions/get-user-package
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fish Audio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fishAudio/latest/actions/get-user-package?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fishAudio/latest/actions/get-user-package?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "balance": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "finished_at": "2026-05-07T12:00:00.000Z",
      "total": 1,
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | number |  |
| `created_at` | date |  |
| `finished_at` | date |  |
| `total` | number |  |
| `type` | string |  |
| `updated_at` | date |  |
| `user_id` | string |  |

## Native endpoint

Through the native Fish Audio API, this operation is `GET /wallet/:user_id/package` (base URL `https://api.fish.audio`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-package.md) for the provider-specific parameters and requirements.

