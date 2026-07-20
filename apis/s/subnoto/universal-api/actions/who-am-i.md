# Subnoto: Who Am I



```
GET https://connect.mindcloud.co/v1/universal/subnoto/latest/actions/who-am-i
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Subnoto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/subnoto/latest/actions/who-am-i?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/subnoto/latest/actions/who-am-i?${params}`, {
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
      "accessKey": "string",
      "agent": {},
      "ownerEmail": "ava@example.com",
      "ownerUuid": "string",
      "teamName": "Ava Chen",
      "teamUuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessKey` | string | The access key used to authenticate the request. |
| `agent` | object | Agent metadata when the request is authenticated as an agent. |
| `ownerEmail` | string | The email address of the team owner. |
| `ownerUuid` | string | The UUID of the team owner. |
| `teamName` | string | The name of the authenticated team. |
| `teamUuid` | string | The UUID of the authenticated team. |

## Native endpoint

Through the native Subnoto API, this operation is `POST /public/utils/whoami` (base URL `https://app.subnoto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/who-am-i.md) for the provider-specific parameters and requirements.

