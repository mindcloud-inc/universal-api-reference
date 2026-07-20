# Workiom: List Views

Retrieves views from your Workiom workspace.

```
GET https://connect.mindcloud.co/v1/universal/workiom/latest/actions/list-views
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Workiom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workiom/latest/actions/list-views?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workiom/latest/actions/list-views?${params}`, {
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
          "accessibility": "string",
          "autoCollapseEnabled": true,
          "creationTime": "2026-05-07T12:00:00.000Z",
          "description": "string",
          "id": 1,
          "isDefault": true,
          "isFieldsEditable": true,
          "lastModificationTime": "2026-05-07T12:00:00.000Z",
          "listId": "string",
          "name": "Ava Chen",
          "order": 1,
          "viewToken": "string",
          "viewType": "string"
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
| `items[].accessibility` | string |  |
| `items[].autoCollapseEnabled` | boolean |  |
| `items[].creationTime` | date |  |
| `items[].description` | string |  |
| `items[].id` | number |  |
| `items[].isDefault` | boolean |  |
| `items[].isFieldsEditable` | boolean |  |
| `items[].lastModificationTime` | date |  |
| `items[].listId` | string |  |
| `items[].name` | string |  |
| `items[].order` | number |  |
| `items[].viewToken` | string |  |
| `items[].viewType` | string |  |

## Native endpoint

Through the native Workiom API, this operation is `GET /api/services/app/Views/GetAll` (base URL `https://api.workiom.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-views.md) for the provider-specific parameters and requirements.

