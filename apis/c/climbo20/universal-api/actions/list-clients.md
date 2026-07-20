# Climbo 2.0: List Clients

Retrieves agency clients from Climbo 2.0.

```
GET https://connect.mindcloud.co/v1/universal/climbo20/latest/actions/list-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Climbo 2.0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/climbo20/latest/actions/list-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/climbo20/latest/actions/list-clients?${params}`, {
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
| `page` | number | no | If not set returns the first page. Default: `1`. |
| `planId` | string | no | Filter by plan ID. |
| `status` | string | no | Filter by customer status. |
| `email` | string | no | Filter by customer email. |

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
| `planId` | string |  |
| `source` | string |  |
| `status` | string |  |
| `userName` | string |  |

## Native endpoint

Through the native Climbo 2.0 API, this operation is `GET /clients` (base URL `https://api.climbo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-clients.md) for the provider-specific parameters and requirements.

