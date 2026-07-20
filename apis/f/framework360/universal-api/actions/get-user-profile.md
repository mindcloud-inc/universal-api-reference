# Framework360: Get User Profile



```
GET https://connect.mindcloud.co/v1/universal/framework360/latest/actions/get-user-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Framework360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/framework360/latest/actions/get-user-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/framework360/latest/actions/get-user-profile?${params}`, {
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
      "active": 1,
      "avatar": "string",
      "cognome": "string",
      "email": "ava@example.com",
      "formatted_name": "Ava Chen",
      "has_wizard": 1,
      "id": "string",
      "nome": "string",
      "ruolo": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | number |  |
| `avatar` | string |  |
| `cognome` | string |  |
| `email` | string |  |
| `formatted_name` | string |  |
| `has_wizard` | number |  |
| `id` | string |  |
| `nome` | string |  |
| `ruolo` | string |  |

## Native endpoint

Through the native Framework360 API, this operation is `GET users/profile` (base URL `https://mindcloudstage0.framework360.site/m/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-profile.md) for the provider-specific parameters and requirements.

