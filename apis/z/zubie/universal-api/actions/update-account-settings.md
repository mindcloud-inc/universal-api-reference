# Zubie: Update Account Settings

Updates account settings in Zubie.

```
PUT https://connect.mindcloud.co/v1/universal/zubie/latest/actions/update-account-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zubie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zubie/latest/actions/update-account-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zubie/latest/actions/update-account-settings', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
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
| `zipcode` | string |  |

## Native endpoint

Through the native Zubie API, this operation is `POST /account` (base URL `https://api.zubiecar.com/api/v2/zinc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-account-settings.md) for the provider-specific parameters and requirements.

