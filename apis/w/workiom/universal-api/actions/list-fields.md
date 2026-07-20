# Workiom: List Fields

Retrieves custom fields from your Workiom workspace.

```
GET https://connect.mindcloud.co/v1/universal/workiom/latest/actions/list-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Workiom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workiom/latest/actions/list-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workiom/latest/actions/list-fields?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "allowMultiple": true,
          "dataType": "string",
          "defaultValue": "string",
          "description": "string",
          "id": "string",
          "isAssociation": true,
          "isComputed": true,
          "isPrimary": true,
          "isRequired": true,
          "isVisible": true,
          "linkedListId": "https://example.com",
          "linkedViewId": 1,
          "listId": "string",
          "name": "Ava Chen",
          "order": 1,
          "summaryType": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[].allowMultiple` | boolean |  |
| `items[].dataType` | string |  |
| `items[].defaultValue` | string |  |
| `items[].description` | string |  |
| `items[].id` | string |  |
| `items[].isAssociation` | boolean |  |
| `items[].isComputed` | boolean |  |
| `items[].isPrimary` | boolean |  |
| `items[].isRequired` | boolean |  |
| `items[].isVisible` | boolean |  |
| `items[].linkedListId` | string |  |
| `items[].linkedViewId` | number |  |
| `items[].listId` | string |  |
| `items[].name` | string |  |
| `items[].order` | number |  |
| `items[].summaryType` | string |  |

## Native endpoint

Through the native Workiom API, this operation is `GET /api/services/app/Fields/GetAll` (base URL `https://api.workiom.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-fields.md) for the provider-specific parameters and requirements.

