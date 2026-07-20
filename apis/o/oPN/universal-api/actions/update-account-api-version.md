# OPN: Update Account API Version

Updates the account API version in OPN.

```
PUT https://connect.mindcloud.co/v1/universal/oPN/latest/actions/update-account-api-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/update-account-api-version" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oPN/latest/actions/update-account-api-version', {
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
      "api_version": "string",
      "country": "string",
      "currency": "string",
      "email": "ava@example.com",
      "id": "string",
      "last_updated_api_version": "string",
      "livemode": true,
      "location": "string",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `api_version` | string |  |
| `country` | string |  |
| `currency` | string |  |
| `email` | string |  |
| `id` | string |  |
| `last_updated_api_version` | string |  |
| `livemode` | boolean |  |
| `location` | string |  |
| `object` | string |  |

## Native endpoint

Through the native OPN API, this operation is `PATCH /account/api_version` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-account-api-version.md) for the provider-specific parameters and requirements.

