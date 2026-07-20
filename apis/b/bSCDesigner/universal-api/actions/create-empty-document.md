# BSC Designer: Create Empty Document



```
POST https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/create-empty-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BSC Designer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/create-empty-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/create-empty-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `parentGroupId` | number | no | Optional parent document group ID for the new empty document. Default: `0`. |

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
| `alias` | string | Document alias. |
| `description` | string | Document description. |
| `guid` | string | Document GUID when available. |
| `icon` | string | Document icon path. |
| `id` | number | Document ID. |
| `items` | array<object> | Child tree items. |
| `name` | string | Document name. |
| `ownerId` | number | Owner user ID. |
| `sharedForPublic` | boolean | Whether the document is public. |
| `sharedForRegRW` | boolean | Whether the document is shared for registered read/write access. |
| `treeGroupId` | number | Parent tree group ID. |
| `type` | string | Document item type returned by BSC Designer. |

## Native endpoint

Through the native BSC Designer API, this operation is `POST /rest/api/documents` (base URL `https://www.webbsc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-empty-document.md) for the provider-specific parameters and requirements.

