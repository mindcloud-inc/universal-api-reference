# NetExplorer: List Quotas



```
GET https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-quotas
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-quotas?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-quotas?${params}`, {
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
      "folder": {
        "folder": 1,
        "quota": "string",
        "used": 1
      },
      "platform": {
        "quota": 1,
        "used": 1
      },
      "user": {
        "quota": "string",
        "used": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `folder.folder` | number |  |
| `folder.quota` | string |  |
| `folder.used` | number |  |
| `platform.quota` | number |  |
| `platform.used` | number |  |
| `user.quota` | string |  |
| `user.used` | number |  |

## Native endpoint

Through the native NetExplorer API, this operation is `GET /quotas` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-quotas.md) for the provider-specific parameters and requirements.

