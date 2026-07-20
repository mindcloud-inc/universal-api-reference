# Chaindesk: List Contacts

Retrieves contacts from your Chaindesk workspace.

```
GET https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chaindesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/list-contacts?${params}`, {
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
      "contacts": {
        "agentId": "string",
        "createdAt": "string",
        "email": "ava@example.com",
        "externalId": "string",
        "firstName": "Ava",
        "id": "string",
        "lastName": "Chen",
        "metadata": "string",
        "organizationId": "string",
        "phoneNumber": "string",
        "updatedAt": "string"
      },
      "count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contacts` | array<object> |  |
| `contacts.agentId` | string |  |
| `contacts.createdAt` | string |  |
| `contacts.email` | string |  |
| `contacts.externalId` | string |  |
| `contacts.firstName` | string |  |
| `contacts.id` | string |  |
| `contacts.lastName` | string |  |
| `contacts.metadata` | string |  |
| `contacts.organizationId` | string |  |
| `contacts.phoneNumber` | string |  |
| `contacts.updatedAt` | string |  |
| `count` | number |  |

## Native endpoint

Through the native Chaindesk API, this operation is `GET /contacts` (base URL `https://app.chaindesk.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

