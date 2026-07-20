# Revel Digital: Update Account



```
PUT https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/update-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Revel Digital `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/update-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/update-account', {
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
      "data": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string | Empty response body returned by the provider for successful no-content updates. |
| `success` | boolean | True when the update request completes successfully. |

## Native endpoint

Through the native Revel Digital API, this operation is `PUT /account` (base URL `https://api.reveldigital.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-account.md) for the provider-specific parameters and requirements.

