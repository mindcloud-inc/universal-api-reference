# Mode: List Collections

List collections that are visible in a Mode workspace.

```
GET https://connect.mindcloud.co/v1/universal/mode/latest/actions/list-collections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mode/latest/actions/list-collections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mode/latest/actions/list-collections?${params}`, {
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
      "defaultAccessLevel": "string",
      "description": "string",
      "Forms": {},
      "freeDefault": true,
      "id": "string",
      "Links": {},
      "name": "Ava Chen",
      "restricted": true,
      "schemaName": "Ava Chen",
      "spaceType": "string",
      "state": "string",
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `defaultAccessLevel` | string | Default collection access level. |
| `description` | string | Collection description. |
| `Forms` | object | Mode HAL forms. |
| `freeDefault` | boolean | Whether the collection is the free default collection. |
| `id` | string | Mode collection ID. |
| `Links` | object | Mode HAL links. |
| `name` | string | Collection name. |
| `restricted` | boolean | Whether the collection is restricted. |
| `schemaName` | string | Collection schema name. |
| `spaceType` | string | Collection type. |
| `state` | string | Collection state. |
| `token` | string | Mode collection token. |

## Native endpoint

Through the native Mode API, this operation is `GET /spaces` (base URL `https://app.mode.com/api/{{credentials.workspace}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-collections.md) for the provider-specific parameters and requirements.

