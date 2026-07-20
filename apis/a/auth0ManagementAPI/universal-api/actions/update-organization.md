# Auth0 Management: Update Organization

Updates an existing organization in Auth0 Management API.

```
PUT https://connect.mindcloud.co/v1/universal/auth0ManagementAPI/latest/actions/update-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Auth0 Management `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/auth0ManagementAPI/latest/actions/update-organization" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/auth0ManagementAPI/latest/actions/update-organization', {
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
      "display_name": "Ava Chen",
      "id": "string",
      "metadata": {},
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `display_name` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `name` | string |  |

## Native endpoint

Through the native Auth0 Management API, this operation is `PATCH /organizations/{id}` (base URL `https://{{credentials.tenantDomain}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-organization.md) for the provider-specific parameters and requirements.

