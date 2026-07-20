# Freshdesk: Get Agent

Retrieves an agent from Freshdesk by ID.

```
GET https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/get-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshdesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/get-agent?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/get-agent?${params}`, {
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
| `id` | list<number> | yes | Freshdesk agent ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "createdAt": "string",
      "email": "ava@example.com",
      "id": 1,
      "jobTitle": "string",
      "name": "Ava Chen",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `createdAt` | string |  |
| `email` | string |  |
| `id` | number |  |
| `jobTitle` | string |  |
| `name` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Freshdesk API, this operation is `GET /agents/:id` (base URL `https://{{credentials.subdomain}}.freshdesk.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agent.md) for the provider-specific parameters and requirements.

