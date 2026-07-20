# Zubie: Get Account Settings

Retrieves account settings from Zubie.

```
GET https://connect.mindcloud.co/v1/universal/zubie/latest/actions/get-account-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zubie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zubie/latest/actions/get-account-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zubie/latest/actions/get-account-settings?${params}`, {
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
      "city": "string",
      "external_id": "string",
      "key": "string",
      "nickname": "Ava Chen",
      "state": "string",
      "street": "string",
      "updated": "string",
      "user_count": 1,
      "zipcode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `external_id` | string |  |
| `key` | string |  |
| `nickname` | string |  |
| `state` | string |  |
| `street` | string |  |
| `updated` | string |  |
| `user_count` | number |  |
| `zipcode` | string |  |

## Native endpoint

Through the native Zubie API, this operation is `GET /account` (base URL `https://api.zubiecar.com/api/v2/zinc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-settings.md) for the provider-specific parameters and requirements.

