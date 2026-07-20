# Crisp: Get Plugin Account

Retrieves your plugin account from Crisp.

```
GET https://connect.mindcloud.co/v1/universal/crisp/latest/actions/get-plugin-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crisp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crisp/latest/actions/get-plugin-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crisp/latest/actions/get-plugin-account?${params}`, {
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
      "pluginId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pluginId` | string |  |

## Native endpoint

Through the native Crisp API, this operation is `GET /plugin/connect/account` (base URL `https://api.crisp.chat/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-plugin-account.md) for the provider-specific parameters and requirements.

