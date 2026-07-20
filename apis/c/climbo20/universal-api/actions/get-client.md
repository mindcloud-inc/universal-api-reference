# Climbo 2.0: Get Client

Retrieves a client from Climbo 2.0.

```
GET https://connect.mindcloud.co/v1/universal/climbo20/latest/actions/get-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Climbo 2.0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/climbo20/latest/actions/get-client?connectionId=$CONNECTION_ID&clientId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clientId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/climbo20/latest/actions/get-client?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | string | yes | ID of your customer. |
| `loginLink` | boolean | no | Whether to return a login link. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "businessName": "Ava Chen",
      "createdAt": "string",
      "email": "ava@example.com",
      "id": "string",
      "locationCount": 1,
      "loginLink": "https://example.com",
      "planId": "string",
      "source": "string",
      "status": "string",
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `businessName` | string |  |
| `createdAt` | string |  |
| `email` | string |  |
| `id` | string |  |
| `locationCount` | number |  |
| `loginLink` | string |  |
| `planId` | string |  |
| `source` | string |  |
| `status` | string |  |
| `userName` | string |  |

## Native endpoint

Through the native Climbo 2.0 API, this operation is `GET /client/{client_id}` (base URL `https://api.climbo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client.md) for the provider-specific parameters and requirements.

