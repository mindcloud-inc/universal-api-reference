# ClickUp: List List Custom Fields

View the Custom Fields in a specific List.

```
GET https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/list-list-custom-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/list-list-custom-fields?connectionId=$CONNECTION_ID&listId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/list-list-custom-fields?${params}`, {
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
| `listId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "hideFromGuests": true,
      "id": "string",
      "name": "Ava Chen",
      "required": true,
      "type": "string",
      "typeConfig": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateCreated` | date |  |
| `hideFromGuests` | boolean |  |
| `id` | string |  |
| `name` | string |  |
| `required` | boolean |  |
| `type` | string |  |
| `typeConfig` | object |  |

## Native endpoint

Through the native ClickUp API, this operation is `GET list/:list_id/field` (base URL `https://api.clickup.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-list-custom-fields.md) for the provider-specific parameters and requirements.

