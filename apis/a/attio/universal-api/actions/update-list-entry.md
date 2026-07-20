# Attio: Update List Entry

Updates a list entry in Attio.

```
PUT https://connect.mindcloud.co/v1/universal/attio/latest/actions/update-list-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Attio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/attio/latest/actions/update-list-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "list": "string",
  "entry_id": "string",
  "entryValues": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/attio/latest/actions/update-list-entry', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "list": "string",
    "entry_id": "string",
    "entryValues": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `list` | string | yes | The UUID or slug identifying the list. |
| `entry_id` | string | yes | The UUID identifying the list entry. |
| `entryValues` | object | yes | Entry values keyed by Attio attribute slug or attribute ID. This overwrite endpoint replaces current multiselect values. |

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

Through the native Attio API, this operation is `PUT /v2/lists/:list/entries/:entry_id` (base URL `https://api.attio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-list-entry.md) for the provider-specific parameters and requirements.

