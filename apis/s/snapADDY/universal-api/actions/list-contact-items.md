# snapADDY: List Contact Items



```
GET https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/list-contact-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a snapADDY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/list-contact-items?connectionId=$CONNECTION_ID&listId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/list-contact-items?${params}`, {
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
| `listId` | string | yes | Contact list identifier |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `page` | number | no | Page number |
| `limit` | number | no | Maximum number of items to return |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        "string"
      ],
      "city": "string",
      "contactListId": "string",
      "country": "string",
      "created": "string",
      "customFields": {},
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "organization": "string",
      "phone": "string",
      "position": "string",
      "updated": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | array<string> |  |
| `city` | string |  |
| `contactListId` | string |  |
| `country` | string |  |
| `created` | string |  |
| `customFields` | object |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `organization` | string |  |
| `phone` | string |  |
| `position` | string |  |
| `updated` | string |  |
| `website` | string |  |

## Native endpoint

Through the native snapADDY API, this operation is `GET /grabber/v1/contactlist/:listId/contactitems` (base URL `https://api.snapaddy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-items.md) for the provider-specific parameters and requirements.

