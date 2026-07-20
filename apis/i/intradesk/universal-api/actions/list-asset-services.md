# Intradesk: List Asset Services

Retrieves services with assets from Intradesk.

```
GET https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/list-asset-services
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intradesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/list-asset-services?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/list-asset-services?${params}`, {
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
      "fullname": "Ava Chen",
      "isadmin": true,
      "name": "Ava Chen",
      "path": "string",
      "settingadminid": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fullname` | string |  |
| `isadmin` | boolean |  |
| `name` | string |  |
| `path` | string |  |
| `settingadminid` | number |  |

## Native endpoint

Through the native Intradesk API, this operation is `GET /changes/api/Services/WithAssetsOnly` (base URL `https://apigw.intradesk.ru`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-asset-services.md) for the provider-specific parameters and requirements.

