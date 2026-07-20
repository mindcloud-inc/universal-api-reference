# Foreplay: Get Usage

Retrieves your Foreplay account usage details.

```
GET https://connect.mindcloud.co/v1/universal/foreplay/latest/actions/get-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Foreplay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/foreplay/latest/actions/get-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/foreplay/latest/actions/get-usage?${params}`, {
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
      "end_date": "2026-05-07T12:00:00.000Z",
      "remaining_credits": 1,
      "start_date": "2026-05-07T12:00:00.000Z",
      "total_credits": 1,
      "user": {
        "email": "ava@example.com",
        "id": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `end_date` | date |  |
| `remaining_credits` | number |  |
| `start_date` | date |  |
| `total_credits` | number |  |
| `user.email` | string |  |
| `user.id` | string |  |

## Native endpoint

Through the native Foreplay API, this operation is `GET /api/usage` (base URL `https://public.api.foreplay.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-usage.md) for the provider-specific parameters and requirements.

