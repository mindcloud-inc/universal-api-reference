# Assembly.com: List Message Channels

Retrieves message channels from Assembly.com.

```
GET https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/list-message-channels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Assembly.com `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/list-message-channels?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/list-message-channels?${params}`, {
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
| `membershipType` | string | no |  |
| `clientId` | string | no | Only return individual channels for this client. |
| `memberId` | string | no | Only return channels that contain the member matching this ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `membershipEntityId` | string | no | Deprecated. Use clientId instead. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "clientId": "string",
          "companyId": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "lastMessageDate": {},
          "memberIds": [
            "string"
          ],
          "membershipEntityId": "string",
          "membershipType": "string",
          "object": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].clientId` | string |  |
| `data[].companyId` | string |  |
| `data[].createdAt` | date |  |
| `data[].id` | string |  |
| `data[].lastMessageDate` | object |  |
| `data[].memberIds[]` | string |  |
| `data[].membershipEntityId` | string |  |
| `data[].membershipType` | string |  |
| `data[].object` | string |  |
| `data[].updatedAt` | date |  |

## Native endpoint

Through the native Assembly.com API, this operation is `GET /message-channels` (base URL `https://api.assembly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-message-channels.md) for the provider-specific parameters and requirements.

