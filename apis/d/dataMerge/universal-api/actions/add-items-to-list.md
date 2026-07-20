# DataMerge: Add Items to List

Adds companies or contacts to a DataMerge list.

```
PUT https://connect.mindcloud.co/v1/universal/dataMerge/latest/actions/add-items-to-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataMerge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dataMerge/latest/actions/add-items-to-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "objectType": "string",
  "list": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dataMerge/latest/actions/add-items-to-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "objectType": "string",
    "list": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `objectType` | string | yes | List object type. |
| `list` | string | yes | List slug. |
| `domains[]` | array<string> | no | Company domains to add to a company list. |
| `contactIds[]` | array<string> | no | Contact record IDs to add to a contact list. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native DataMerge API returns.

## Native endpoint

Through the native DataMerge API, this operation is `POST /v1/lists/:object_type/:list/add` (base URL `https://api.datamerge.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-items-to-list.md) for the provider-specific parameters and requirements.

