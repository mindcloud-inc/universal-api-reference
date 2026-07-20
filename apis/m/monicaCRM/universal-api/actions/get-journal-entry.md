# Monica CRM: Get Journal Entry

Retrieves a journal entry from Monica CRM.

```
GET https://connect.mindcloud.co/v1/universal/monicaCRM/latest/actions/get-journal-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Monica CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monicaCRM/latest/actions/get-journal-entry?connectionId=$CONNECTION_ID&journalEntryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "journalEntryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monicaCRM/latest/actions/get-journal-entry?${params}`, {
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
| `journalEntryId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "contact": {
          "id": 1
        },
        "created_at": "string",
        "description": "string",
        "happened_at": "string",
        "id": 1,
        "object": "string",
        "title": "string",
        "updated_at": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.contact.id` | number |  |
| `data.created_at` | string |  |
| `data.description` | string |  |
| `data.happened_at` | string |  |
| `data.id` | number |  |
| `data.object` | string |  |
| `data.title` | string |  |
| `data.updated_at` | string |  |

## Native endpoint

Through the native Monica CRM API, this operation is `GET /journal/:journalEntryId` (base URL `https://app.monicahq.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-journal-entry.md) for the provider-specific parameters and requirements.

