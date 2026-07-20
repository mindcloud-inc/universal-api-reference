# Timekit: Get Current App

Retrieves the current app from Timekit.

```
GET https://connect.mindcloud.co/v1/universal/timekit/latest/actions/get-current-app
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timekit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timekit/latest/actions/get-current-app?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timekit/latest/actions/get-current-app?${params}`, {
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
      "api_trial_expires_at": "2026-05-07T12:00:00.000Z",
      "created_at": "2026-05-07T12:00:00.000Z",
      "creator_resource_id": "string",
      "id": "string",
      "role": "string",
      "settings": {},
      "slug": "string",
      "test_mode": true,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "webhook_secret": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `api_trial_expires_at` | date |  |
| `created_at` | date |  |
| `creator_resource_id` | string |  |
| `id` | string |  |
| `role` | string |  |
| `settings` | object |  |
| `slug` | string |  |
| `test_mode` | boolean |  |
| `updated_at` | date |  |
| `webhook_secret` | string |  |

## Native endpoint

Through the native Timekit API, this operation is `GET /app` (base URL `https://api.timekit.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-app.md) for the provider-specific parameters and requirements.

