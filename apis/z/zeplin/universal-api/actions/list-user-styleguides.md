# Zeplin: List User Styleguides

Retrieves a list of user styleguides from Zeplin.

```
GET https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-user-styleguides
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-user-styleguides?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-user-styleguides?${params}`, {
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
| `status` | string | no | Filter by status |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": 1,
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "number_of_colors": 1,
      "number_of_components": 1,
      "number_of_connected_components": 1,
      "number_of_members": 1,
      "number_of_text_styles": 1,
      "parent": {},
      "platform": "string",
      "status": "string",
      "thumbnail": "string",
      "updated": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | number |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `number_of_colors` | number |  |
| `number_of_components` | number |  |
| `number_of_connected_components` | number |  |
| `number_of_members` | number |  |
| `number_of_text_styles` | number |  |
| `parent` | object |  |
| `platform` | string |  |
| `status` | string |  |
| `thumbnail` | string |  |
| `updated` | number |  |

## Native endpoint

Through the native Zeplin API, this operation is `GET /users/me/styleguides` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-user-styleguides.md) for the provider-specific parameters and requirements.

