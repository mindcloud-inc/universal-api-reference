# Codemagic: Get User Preferences

Retrieves preferences for the authenticated Codemagic user.

```
GET https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/get-user-preferences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codemagic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/get-user-preferences?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/get-user-preferences?${params}`, {
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
      "pinned_accounts": [
        {}
      ],
      "theme": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pinned_accounts` | array<object> |  |
| `theme` | string |  |

## Native endpoint

Through the native Codemagic API, this operation is `GET /api/v3/user/preferences` (base URL `https://codemagic.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-preferences.md) for the provider-specific parameters and requirements.

