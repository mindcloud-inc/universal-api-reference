# Botsonic: List Starter Presets

Retrieves all starter presets from Botsonic.

```
GET https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/list-starter-presets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Botsonic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/list-starter-presets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/list-starter-presets?${params}`, {
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
      "starter_questions": [
        {}
      ],
      "welcome_message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `starter_questions` | array<object> | Starter question presets. |
| `welcome_message` | string | Welcome message preset. |

## Native endpoint

Through the native Botsonic API, this operation is `GET /v1/business/bot-starter-presets/all` (base URL `https://api.botsonic.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-starter-presets.md) for the provider-specific parameters and requirements.

