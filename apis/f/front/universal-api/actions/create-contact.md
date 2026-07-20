# Front: Create Contact

Creates a new contact in Front.

```
POST https://connect.mindcloud.co/v1/universal/front/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Front `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/front/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "handles[]": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/front/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "handles[]": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Example: `Stage 3 Test Contact`. |
| `description` | string | no | Example: `Created during Front Stage 3 buildout`. |
| `handles[]` | array<object> | yes | JSON array of Front handle objects, for example [{"handle":"person@example.com","source":"email"}]. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `avatar` | file | no |  |
| `links[]` | array<string> | no | Example: `https://example.com`. |
| `groupNames[]` | array<string> | no | Deprecated by Front. Prefer `list_names`. Example: `Customers`. |
| `listNames[]` | array<string> | no | Example: `VIP`. |
| `customFields` | object | no | Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": {},
      "avatarUrl": {},
      "description": "string",
      "handles": [
        {
          "handle": "string",
          "source": "string"
        }
      ],
      "id": "string",
      "isPrivate": true,
      "links": {
        "related": {
          "conversations": "https://example.com",
          "notes": "https://example.com",
          "owner": {}
        },
        "self": "https://example.com"
      },
      "name": "Ava Chen",
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | object |  |
| `avatarUrl` | object |  |
| `description` | string |  |
| `handles[].handle` | string |  |
| `handles[].source` | string |  |
| `id` | string |  |
| `isPrivate` | boolean |  |
| `links.related.conversations` | string |  |
| `links.related.notes` | string |  |
| `links.related.owner` | object |  |
| `links.self` | string |  |
| `name` | string |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native Front API, this operation is `POST /contacts` (base URL `https://api2.frontapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

