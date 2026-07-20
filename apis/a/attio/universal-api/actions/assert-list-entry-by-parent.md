# Attio: Assert List Entry by Parent

Creates or updates a list entry in Attio by parent record.

```
PUT https://connect.mindcloud.co/v1/universal/attio/latest/actions/assert-list-entry-by-parent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Attio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/attio/latest/actions/assert-list-entry-by-parent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "list": "string",
  "parentObject": "string",
  "parentRecordId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/attio/latest/actions/assert-list-entry-by-parent', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "list": "string",
    "parentObject": "string",
    "parentRecordId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `list` | string | yes | The UUID or slug identifying the list. |
| `parentObject` | string<string> | yes | The parent object slug or UUID used to identify the list entry by parent record. |
| `parentRecordId` | string | yes | The record ID used to identify the list entry by parent record. |
| `entryValues` | object | no | Optional list entry values keyed by Attio attribute slug or attribute ID. |

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

Through the native Attio API, this operation is `PUT /v2/lists/:list/entries` (base URL `https://api.attio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assert-list-entry-by-parent.md) for the provider-specific parameters and requirements.

