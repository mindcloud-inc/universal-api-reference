# WhautoChat: Get Contact Tag by ID

Retrieves a contact tag from WhautoChat by ID.

```
GET https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/get-contact-tag-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhautoChat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/get-contact-tag-by-id?connectionId=$CONNECTION_ID&contactTagId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactTagId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/get-contact-tag-by-id?${params}`, {
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
| `contactTagId` | string | yes | Contact tag unique ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canonical": "string",
      "createdAt": "string",
      "id": "string",
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canonical` | string |  |
| `createdAt` | string |  |
| `id` | string |  |
| `name` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native WhautoChat API, this operation is `GET /v1/contactTags/{contactTagId}` (base URL `https://api.whauto.chat`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-tag-by-id.md) for the provider-specific parameters and requirements.

