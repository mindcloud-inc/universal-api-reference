# Refiner: List Contacts

Retrieves contacts from your Refiner account.

```
GET https://connect.mindcloud.co/v1/universal/refiner/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Refiner `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/refiner/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/refiner/latest/actions/list-contacts?${params}`, {
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
| `search` | string | no | Search contact email, ID, or name. |
| `formUuid` | string | no | Only include contacts linked to a specific survey. |
| `segmentUuid` | string | no | Only include contacts matching a specific segment. |
| `orderBy` | string | no | Sort contacts by first_seen_at, last_seen_at, or last_form_submission_at. |
| `pageCursor` | string | no | Cursor for the next contacts page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": {},
      "attributes": {},
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "firstSeenAt": "2026-05-07T12:00:00.000Z",
      "lastSeenAt": "2026-05-07T12:00:00.000Z",
      "remoteId": "string",
      "segments": [
        {}
      ],
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | object |  |
| `attributes` | object |  |
| `displayName` | string |  |
| `email` | string |  |
| `firstSeenAt` | date |  |
| `lastSeenAt` | date |  |
| `remoteId` | string |  |
| `segments` | array<object> |  |
| `uuid` | string |  |

## Native endpoint

Through the native Refiner API, this operation is `GET /contacts` (base URL `https://api.refiner.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

