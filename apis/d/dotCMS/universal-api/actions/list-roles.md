# DotCMS: List Roles

Retrieves root role records from DotCMS.

```
GET https://connect.mindcloud.co/v1/universal/dotCMS/latest/actions/list-roles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DotCMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dotCMS/latest/actions/list-roles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dotCMS/latest/actions/list-roles?${params}`, {
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
      "entity": [
        {
          "dbfqn": "string",
          "description": "string",
          "editLayouts": true,
          "editPermissions": true,
          "editUsers": true,
          "fqn": "string",
          "id": "string",
          "locked": true,
          "name": "Ava Chen",
          "parent": "string",
          "roleChildren": [
            {
              "dbfqn": "string",
              "description": "string",
              "editLayouts": true,
              "editPermissions": true,
              "editUsers": true,
              "fqn": "string",
              "id": "string",
              "locked": true,
              "name": "Ava Chen",
              "parent": "string",
              "roleKey": "string",
              "system": true
            }
          ],
          "roleKey": {},
          "system": true
        }
      ],
      "pagination": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entity[].dbfqn` | string |  |
| `entity[].description` | string |  |
| `entity[].editLayouts` | boolean |  |
| `entity[].editPermissions` | boolean |  |
| `entity[].editUsers` | boolean |  |
| `entity[].fqn` | string |  |
| `entity[].id` | string |  |
| `entity[].locked` | boolean |  |
| `entity[].name` | string |  |
| `entity[].parent` | string |  |
| `entity[].roleChildren[].dbfqn` | string |  |
| `entity[].roleChildren[].description` | string |  |
| `entity[].roleChildren[].editLayouts` | boolean |  |
| `entity[].roleChildren[].editPermissions` | boolean |  |
| `entity[].roleChildren[].editUsers` | boolean |  |
| `entity[].roleChildren[].fqn` | string |  |
| `entity[].roleChildren[].id` | string |  |
| `entity[].roleChildren[].locked` | boolean |  |
| `entity[].roleChildren[].name` | string |  |
| `entity[].roleChildren[].parent` | string |  |
| `entity[].roleChildren[].roleKey` | string |  |
| `entity[].roleChildren[].system` | boolean |  |
| `entity[].roleKey` | object |  |
| `entity[].system` | boolean |  |
| `pagination` | object |  |

## Native endpoint

Through the native DotCMS API, this operation is `GET /api/v1/roles` (base URL `https://demo.dotcms.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-roles.md) for the provider-specific parameters and requirements.

