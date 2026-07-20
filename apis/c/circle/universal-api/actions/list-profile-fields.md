# Circle: List Profile Fields

Retrieves profile field records from Circle.

```
GET https://connect.mindcloud.co/v1/universal/circle/latest/actions/list-profile-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Circle `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/circle/latest/actions/list-profile-fields?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/circle/latest/actions/list-profile-fields?${params}`, {
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
      "allowNull": true,
      "archived": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "fieldType": "string",
      "id": 1,
      "key": "string",
      "label": "string",
      "numberOptions": "string",
      "pages": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "id": 1,
          "name": "Ava Chen",
          "position": 1,
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "visible": true
        }
      ],
      "placeholder": "string",
      "platformField": true,
      "required": true,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowNull` | boolean |  |
| `archived` | boolean |  |
| `createdAt` | date |  |
| `description` | string |  |
| `fieldType` | string |  |
| `id` | number |  |
| `key` | string |  |
| `label` | string |  |
| `numberOptions` | string |  |
| `pages[].createdAt` | date |  |
| `pages[].id` | number |  |
| `pages[].name` | string |  |
| `pages[].position` | number |  |
| `pages[].updatedAt` | date |  |
| `pages[].visible` | boolean |  |
| `placeholder` | string |  |
| `platformField` | boolean |  |
| `required` | boolean |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Circle API, this operation is `GET /api/admin/v2/profile_fields` (base URL `https://{{credentials.subdomain}}.circle.so`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-profile-fields.md) for the provider-specific parameters and requirements.

