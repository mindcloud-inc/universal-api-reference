# Zeplin: List Styleguide Connected Components

Retrieves a list of styleguide connected components from Zeplin.

```
GET https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-styleguide-connected-components
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-styleguide-connected-components?connectionId=$CONNECTION_ID&limit=25&offset=0&styleguideId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "styleguideId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-styleguide-connected-components?${params}`, {
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
| `styleguideId` | string | yes | Styleguide id |
| `linkedProject` | string | no | Reference project id |
| `linkedStyleguide` | string | no | Reference styleguide id |
| `includeLinkedStyleguides` | boolean | no | Whether to include linked styleguides or not |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": {},
      "components": [
        {}
      ],
      "description": "string",
      "links": [
        {}
      ],
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | object |  |
| `components` | array<object> |  |
| `description` | string |  |
| `links` | array<object> |  |
| `name` | string |  |

## Native endpoint

Through the native Zeplin API, this operation is `GET /styleguides/{styleguide_id}/connected_components` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-styleguide-connected-components.md) for the provider-specific parameters and requirements.

