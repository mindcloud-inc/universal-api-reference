# Digiclose: List Contact Tasks



```
GET https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/list-contact-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digiclose `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/list-contact-tasks?connectionId=$CONNECTION_ID&contactId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/list-contact-tasks?${params}`, {
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
| `contactId` | number | yes | Unique identifier for the contact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assigneeId": 1,
      "categoryName": "Ava Chen",
      "completedAt": {},
      "contactId": 1,
      "creatorId": 1,
      "description": "string",
      "dueAt": "string",
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assigneeId` | number |  |
| `categoryName` | string |  |
| `completedAt` | object |  |
| `contactId` | number |  |
| `creatorId` | number |  |
| `description` | string |  |
| `dueAt` | string |  |
| `id` | number |  |

## Native endpoint

Through the native Digiclose API, this operation is `GET /contacts/:contact_id/tasks` (base URL `https://app.digiclose.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-tasks.md) for the provider-specific parameters and requirements.

