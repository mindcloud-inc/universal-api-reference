# vPlan: Retrieve Authentication Details



```
GET https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/retrieve-authentication-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a vPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/retrieve-authentication-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/retrieve-authentication-details?${params}`, {
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
      "api-key": {},
      "board_permission_set": {},
      "environment": {},
      "features": [
        "string"
      ],
      "host": {},
      "next": true,
      "settings": [
        {}
      ],
      "show_nps": true,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `api-key` | object | API key metadata. |
| `board_permission_set` | object | Board permission map. |
| `environment` | object | Environment metadata. |
| `features` | array<string> | Enabled features. |
| `host` | object | Host metadata. |
| `next` | boolean | Whether a next onboarding step is available. |
| `settings` | array<object> | Environment settings. |
| `show_nps` | boolean | Whether NPS is shown. |
| `type` | string | Authentication type. |

## Native endpoint

Through the native vPlan API, this operation is `GET /me` (base URL `https://api.vplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-authentication-details.md) for the provider-specific parameters and requirements.

