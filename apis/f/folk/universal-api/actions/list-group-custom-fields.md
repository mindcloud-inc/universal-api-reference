# folk: List Group Custom Fields

Retrieves group custom fields for an entity type in folk.

```
GET https://connect.mindcloud.co/v1/universal/folk/latest/actions/list-group-custom-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a folk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/folk/latest/actions/list-group-custom-fields?connectionId=$CONNECTION_ID&limit=25&offset=0&entityType=string&groupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "entityType": "string",
  "groupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/folk/latest/actions/list-group-custom-fields?${params}`, {
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
| `entityType` | string | yes | The entity type for the group's custom fields, such as person or company. |
| `groupId` | string | yes | The ID of the group whose custom fields you want to list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "config": {},
      "name": "Ava Chen",
      "options": [
        {}
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `config` | object |  |
| `name` | string |  |
| `options` | array<object> |  |
| `type` | string |  |

## Native endpoint

Through the native folk API, this operation is `GET /v1/groups/:groupId/custom-fields/:entityType` (base URL `https://api.folk.app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-group-custom-fields.md) for the provider-specific parameters and requirements.

