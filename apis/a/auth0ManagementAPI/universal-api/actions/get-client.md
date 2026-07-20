# Auth0 Management: Get Client

Retrieves a client from Auth0 Management API.

```
GET https://connect.mindcloud.co/v1/universal/auth0ManagementAPI/latest/actions/get-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Auth0 Management `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/auth0ManagementAPI/latest/actions/get-client?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/auth0ManagementAPI/latest/actions/get-client?${params}`, {
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

Through the native Auth0 Management API, this operation is `GET /clients/{id}` (base URL `https://{{credentials.tenantDomain}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client.md) for the provider-specific parameters and requirements.

