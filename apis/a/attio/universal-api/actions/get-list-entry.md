# Attio: Get List Entry

Retrieves a list entry from Attio.

```
GET https://connect.mindcloud.co/v1/universal/attio/latest/actions/get-list-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Attio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/attio/latest/actions/get-list-entry?connectionId=$CONNECTION_ID&list=string&entry_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "list": "string",
  "entry_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/attio/latest/actions/get-list-entry?${params}`, {
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
| `list` | string | yes | The UUID or slug identifying the list. |
| `entry_id` | string | yes | The UUID identifying the list entry. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "entryValues": {},
      "id": {},
      "parentObject": "string",
      "parentRecordId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | When the list entry was created. |
| `entryValues` | object | Dynamic list-entry values keyed by Attio attribute slug or id. |
| `id` | object | List entry identifier payload containing workspace, list, and entry ids. |
| `parentObject` | string | Parent object slug for the entry. |
| `parentRecordId` | string | Parent record id linked to the entry. |

## Native endpoint

Through the native Attio API, this operation is `GET /v2/lists/:list/entries/:entry_id` (base URL `https://api.attio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list-entry.md) for the provider-specific parameters and requirements.

