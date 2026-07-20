# MENU TIGER: Get Integration Status



```
GET https://connect.mindcloud.co/v1/universal/mENUTIGER/latest/actions/get-integration-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MENU TIGER `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mENUTIGER/latest/actions/get-integration-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mENUTIGER/latest/actions/get-integration-status?${params}`, {
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
      "data": {
        "name": "Ava Chen",
        "restaurantUrl": "https://example.com"
      },
      "msg": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Integration status payload. |
| `data.name` | string | Restaurant name returned by MENU TIGER. |
| `data.restaurantUrl` | string | Restaurant URL slug returned by MENU TIGER. |
| `msg` | string | Provider status message. |
| `success` | boolean | Whether the MENU TIGER integration status call succeeded. |

## Native endpoint

Through the native MENU TIGER API, this operation is `GET /zapier/status` (base URL `https://alb.menutigr.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-integration-status.md) for the provider-specific parameters and requirements.

