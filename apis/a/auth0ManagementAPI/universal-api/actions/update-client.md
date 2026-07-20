# Auth0 Management: Update Client

Updates an existing client in Auth0 Management API.

```
PUT https://connect.mindcloud.co/v1/universal/auth0ManagementAPI/latest/actions/update-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Auth0 Management `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/auth0ManagementAPI/latest/actions/update-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/auth0ManagementAPI/latest/actions/update-client', {
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
      "app_type": "string",
      "client_id": "string",
      "description": "string",
      "is_first_party": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `app_type` | string |  |
| `client_id` | string |  |
| `description` | string |  |
| `is_first_party` | boolean |  |
| `name` | string |  |

## Native endpoint

Through the native Auth0 Management API, this operation is `PATCH /clients/{id}` (base URL `https://{{credentials.tenantDomain}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-client.md) for the provider-specific parameters and requirements.

