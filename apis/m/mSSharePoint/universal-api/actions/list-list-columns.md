# MS SharePoint: List List Columns

Retrieves columns from a SharePoint list.

```
GET https://connect.mindcloud.co/v1/universal/mSSharePoint/latest/actions/list-list-columns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MS SharePoint `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mSSharePoint/latest/actions/list-list-columns?connectionId=$CONNECTION_ID&limit=25&offset=0&siteId=string&listId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "siteId": "string",
  "listId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mSSharePoint/latest/actions/list-list-columns?${params}`, {
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
| `siteId` | string | yes | Microsoft Graph SharePoint site ID. |
| `listId` | string | yes | SharePoint list ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "choice": {},
      "columnGroup": "string",
      "dateTime": {},
      "description": "string",
      "displayName": "Ava Chen",
      "hidden": true,
      "id": "string",
      "indexed": true,
      "lookup": {},
      "name": "Ava Chen",
      "number": {},
      "readOnly": true,
      "required": true,
      "text": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `choice` | object |  |
| `columnGroup` | string |  |
| `dateTime` | object |  |
| `description` | string |  |
| `displayName` | string |  |
| `hidden` | boolean |  |
| `id` | string |  |
| `indexed` | boolean |  |
| `lookup` | object |  |
| `name` | string |  |
| `number` | object |  |
| `readOnly` | boolean |  |
| `required` | boolean |  |
| `text` | object |  |

## Native endpoint

Through the native MS SharePoint API, this operation is `GET /v1.0/sites/{{siteId}}/lists/{{listId}}/columns` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-list-columns.md) for the provider-specific parameters and requirements.

