# ProjectManager: Retrieve Project Templates

Retrieves project templates from ProjectManager.

```
GET https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/retrieve-project-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProjectManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/retrieve-project-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/retrieve-project-templates?${params}`, {
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
      "createDate": "string",
      "defaultView": "string",
      "description": "string",
      "icon": "string",
      "id": "string",
      "isCustom": true,
      "name": "Ava Chen",
      "order": 1,
      "ownerId": "string",
      "previewImage": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createDate` | string |  |
| `defaultView` | string |  |
| `description` | string |  |
| `icon` | string |  |
| `id` | string |  |
| `isCustom` | boolean |  |
| `name` | string |  |
| `order` | number |  |
| `ownerId` | string |  |
| `previewImage` | string |  |
| `title` | string |  |

## Native endpoint

Through the native ProjectManager API, this operation is `GET /api/data/projects/templates` (base URL `https://api.projectmanager.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-project-templates.md) for the provider-specific parameters and requirements.

