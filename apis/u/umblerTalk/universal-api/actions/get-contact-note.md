# Umbler Talk: Get Contact Note

Retrieves a contact note from Umbler Talk.

```
GET https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/get-contact-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umbler Talk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/get-contact-note?connectionId=$CONNECTION_ID&id=string&noteId=string&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "noteId": "string",
  "organizationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/get-contact-note?${params}`, {
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
| `id` | string | yes | The contact ID. |
| `noteId` | string | yes | The note ID. |
| `organizationId` | string | yes | The organization ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_t": "string",
      "content": "string",
      "createdAtUTC": "2026-05-07T12:00:00.000Z",
      "createdBy": {},
      "elements": [
        {}
      ],
      "id": "string",
      "mentions": [
        {}
      ],
      "pinned": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_t` | string |  |
| `content` | string |  |
| `createdAtUTC` | date |  |
| `createdBy` | object |  |
| `elements` | array<object> |  |
| `id` | string |  |
| `mentions` | array<object> |  |
| `pinned` | boolean |  |

## Native endpoint

Through the native Umbler Talk API, this operation is `GET /v1/contacts/[:id]/note/[:noteId]/` (base URL `https://app-utalk.umbler.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-note.md) for the provider-specific parameters and requirements.

