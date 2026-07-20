# Split CSV: Retrieve Profile

Retrieves the current user profile from Split CSV.

```
GET https://connect.mindcloud.co/v1/universal/splitCSV/latest/actions/retrieve-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Split CSV `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/splitCSV/latest/actions/retrieve-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/splitCSV/latest/actions/retrieve-profile?${params}`, {
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
      "defaultRetention": 1,
      "email": "ava@example.com",
      "name": "Ava Chen",
      "perFileNotifications": true,
      "provider": "string",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `defaultRetention` | number | The default retention period in days. |
| `email` | string | The account email address. |
| `name` | string | The account display name. |
| `perFileNotifications` | boolean | Whether per-file webhook notifications are enabled. |
| `provider` | string | The account authentication provider. |
| `timezone` | string | The account timezone. |

## Native endpoint

Through the native Split CSV API, this operation is `GET /app/v1/account/profile` (base URL `https://www.splitcsv.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-profile.md) for the provider-specific parameters and requirements.

