# Fish Audio: Get API Credit

Retrieves current API credit balance from Fish Audio.

```
GET https://connect.mindcloud.co/v1/universal/fishAudio/latest/actions/get-api-credit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fish Audio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fishAudio/latest/actions/get-api-credit?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fishAudio/latest/actions/get-api-credit?${params}`, {
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
| `checkFreeCredit` | boolean | no | When true, also returns free-credit availability. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "credit": "string",
      "has_free_credit": true,
      "has_phone_sha256": true,
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
| `_id` | string |  |
| `created_at` | date |  |
| `credit` | string |  |
| `has_free_credit` | boolean |  |
| `has_phone_sha256` | boolean |  |
| `updated_at` | date |  |
| `user_id` | string |  |

## Native endpoint

Through the native Fish Audio API, this operation is `GET /wallet/:user_id/api-credit` (base URL `https://api.fish.audio`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-credit.md) for the provider-specific parameters and requirements.

