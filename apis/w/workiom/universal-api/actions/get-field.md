# Workiom: Get Field

Retrieves a custom field from your Workiom workspace.

```
GET https://connect.mindcloud.co/v1/universal/workiom/latest/actions/get-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Workiom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workiom/latest/actions/get-field?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workiom/latest/actions/get-field?${params}`, {
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

Through the native Workiom API, this operation is `GET /api/services/app/Fields/Get` (base URL `https://api.workiom.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-field.md) for the provider-specific parameters and requirements.

