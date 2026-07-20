# Clio Grow: List Contact Notes



```
GET https://connect.mindcloud.co/v1/universal/clioGrow/latest/actions/list-contact-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clio Grow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clioGrow/latest/actions/list-contact-notes?connectionId=$CONNECTION_ID&limit=25&offset=0&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clioGrow/latest/actions/list-contact-notes?${params}`, {
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
| `contactId` | string | yes | The unique identifier for the contact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "subject": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string |  |
| `createdAt` | date |  |
| `id` | number |  |
| `subject` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Clio Grow API, this operation is `GET /contacts/{contact_id}/notes` (base URL `https://api.clio.com/grow`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contact-notes.md) for the provider-specific parameters and requirements.

