# BSC Designer: Update Document



```
PUT https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/update-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BSC Designer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/update-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/update-document', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Document id to update. |
| `name` | string | yes | Updated document name. |
| `alias` | string | no | Updated document alias. |
| `description` | string | no | Updated document description. |
| `sharedForPublic` | boolean | no | Whether the document is shared publicly. |
| `sharedForRegRW` | boolean | no | Whether the document is shared with registered users as read/write. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "description": "string",
      "guid": "string",
      "icon": "string",
      "id": 1,
      "items": [
        {}
      ],
      "name": "Ava Chen",
      "ownerId": 1,
      "sharedForPublic": true,
      "sharedForRegRW": true,
      "treeGroupId": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string |  |
| `description` | string |  |
| `guid` | string |  |
| `icon` | string |  |
| `id` | number |  |
| `items` | array<object> |  |
| `name` | string |  |
| `ownerId` | number |  |
| `sharedForPublic` | boolean |  |
| `sharedForRegRW` | boolean |  |
| `treeGroupId` | number |  |
| `type` | string |  |

## Native endpoint

Through the native BSC Designer API, this operation is `PUT /rest/api/documents/list/:id` (base URL `https://www.webbsc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-document.md) for the provider-specific parameters and requirements.

