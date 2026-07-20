# Workiom: Create Field

Creates a new custom field in Workiom.

```
POST https://connect.mindcloud.co/v1/universal/workiom/latest/actions/create-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Workiom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/workiom/latest/actions/create-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workiom/latest/actions/create-field', {
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



## Response

```json
{
  "success": true,
  "data": [
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowMultiple` | boolean |  |
| `dataType` | string |  |
| `defaultValue` | string |  |
| `description` | string |  |
| `id` | string |  |
| `isAssociation` | boolean |  |
| `isComputed` | boolean |  |
| `isPrimary` | boolean |  |
| `isRequired` | boolean |  |
| `isVisible` | boolean |  |
| `linkedListId` | string |  |
| `linkedViewId` | number |  |
| `listId` | string |  |
| `name` | string |  |
| `order` | number |  |
| `summaryType` | string |  |

## Native endpoint

Through the native Workiom API, this operation is `POST /api/services/app/Fields/Create` (base URL `https://api.workiom.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-field.md) for the provider-specific parameters and requirements.

