# Datalyse: Get All Agents

Retrieves all company agents from Datalyse.

```
GET https://connect.mindcloud.co/v1/universal/datalyse/latest/actions/get-all-agents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datalyse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datalyse/latest/actions/get-all-agents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datalyse/latest/actions/get-all-agents?${params}`, {
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
      "agentId": "string",
      "avatar": "string",
      "email": "ava@example.com",
      "language": "string",
      "lastname": "Chen",
      "name": "Ava Chen",
      "phone": "string",
      "role": "string",
      "status": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentId` | string | Datalyse agent identifier. |
| `avatar` | string | Agent avatar URL or path. |
| `email` | string | Agent email address. |
| `language` | string | Agent language code. |
| `lastname` | string | Agent last name. |
| `name` | string | Agent first name. |
| `phone` | string | Agent phone number. |
| `role` | string | Agent role label. |
| `status` | string | Agent status label. |
| `username` | string | Agent username. |

## Native endpoint

Through the native Datalyse API, this operation is `POST /api/1.0/companyuserdata/getallagents.json` (base URL `https://api.datalyse.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-agents.md) for the provider-specific parameters and requirements.

