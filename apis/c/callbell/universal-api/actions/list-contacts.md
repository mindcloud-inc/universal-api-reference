# Callbell: List Contacts

Retrieves contacts for the current Callbell account.

```
GET https://connect.mindcloud.co/v1/universal/callbell/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Callbell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callbell/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callbell/latest/actions/list-contacts?${params}`, {
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
| `includeFieldTypes` | boolean | no | Include custom field metadata in the response. |
| `page` | number | no | Page number to retrieve. |
| `source` | string | no | Filter contacts by integration source such as whatsapp. |
| `tags` | string | no | Comma-separated list of tags to match. |
| `teamUuid` | string | no | Filter contacts by team UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedUser": {},
      "avatarUrl": "https://example.com",
      "blockedAt": "string",
      "channel": {},
      "closedAt": "string",
      "conversationHref": "string",
      "createdAt": "string",
      "customFields": {},
      "funnelId": "string",
      "href": "string",
      "name": "Ava Chen",
      "phoneNumber": "string",
      "source": "string",
      "tags": [
        "string"
      ],
      "team": {},
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedUser` | object |  |
| `avatarUrl` | string |  |
| `blockedAt` | string |  |
| `channel` | object |  |
| `closedAt` | string |  |
| `conversationHref` | string |  |
| `createdAt` | string |  |
| `customFields` | object |  |
| `funnelId` | string |  |
| `href` | string |  |
| `name` | string |  |
| `phoneNumber` | string |  |
| `source` | string |  |
| `tags` | array<string> |  |
| `team` | object |  |
| `uuid` | string |  |

## Native endpoint

Through the native Callbell API, this operation is `GET /contacts` (base URL `https://api.callbell.eu/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

