# WEEEK: List Organizations



```
GET https://connect.mindcloud.co/v1/universal/wEEEK/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WEEEK `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wEEEK/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wEEEK/latest/actions/list-organizations?${params}`, {
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
      "organizations": [
        {}
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `organizations` | array<object> | The organizations returned by WEEEK. |
| `success` | boolean | Whether the request succeeded. |

## Native endpoint

Through the native WEEEK API, this operation is `GET /crm/organizations` (base URL `https://api.weeek.net/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

