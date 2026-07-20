# Histre: Retrieve User Settings

Retrieves user settings from Histre.

```
GET https://connect.mindcloud.co/v1/universal/histre/latest/actions/retrieve-user-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Histre `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/histre/latest/actions/retrieve-user-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/histre/latest/actions/retrieve-user-settings?${params}`, {
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
      "email": "ava@example.com",
      "external_id": "string",
      "history": true,
      "org_name": "Ava Chen",
      "pagesize": 1,
      "plan": "string",
      "tz": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Email address on the current Histre account. |
| `external_id` | string | External identifier for the current user. |
| `history` | boolean | Whether history tracking is enabled. |
| `org_name` | string | Organization name when present. |
| `pagesize` | number | Preferred page size setting. |
| `plan` | string | Current subscription plan. |
| `tz` | string | Configured timezone for the current user. |
| `username` | string | Current Histre username. |

## Native endpoint

Through the native Histre API, this operation is `GET /api/v1/settings/` (base URL `https://histre.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-user-settings.md) for the provider-specific parameters and requirements.

