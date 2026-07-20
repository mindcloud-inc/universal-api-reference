# WhautoChat: Get Contact by ID

Retrieves a contact from WhautoChat by ID.

```
GET https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/get-contact-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhautoChat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/get-contact-by-id?connectionId=$CONNECTION_ID&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/get-contact-by-id?${params}`, {
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
| `contactId` | string | yes | Contact unique ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customFields": {},
      "id": "string",
      "name": "Ava Chen",
      "notes": "string",
      "phoneNumber": "string",
      "stage": "string",
      "tags": [
        "string"
      ],
      "workspace": {
        "id": "string",
        "title": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customFields` | object |  |
| `id` | string |  |
| `name` | string |  |
| `notes` | string |  |
| `phoneNumber` | string |  |
| `stage` | string |  |
| `tags` | array<string> |  |
| `workspace.id` | string |  |
| `workspace.title` | string |  |

## Native endpoint

Through the native WhautoChat API, this operation is `GET /v1/contacts/{contactId}` (base URL `https://api.whauto.chat`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-by-id.md) for the provider-specific parameters and requirements.

