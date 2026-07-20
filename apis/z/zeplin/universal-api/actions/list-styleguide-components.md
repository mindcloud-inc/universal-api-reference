# Zeplin: List Styleguide Components

Retrieves a list of styleguide components from Zeplin.

```
GET https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-styleguide-components
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-styleguide-components?connectionId=$CONNECTION_ID&limit=25&offset=0&styleguideId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "styleguideId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-styleguide-components?${params}`, {
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
| `sectionId` | string | no | Filter by section id |
| `sort` | string | no | Sort components by their `section` or their `created` date |
| `linkedProject` | string | no | Reference project id |
| `linkedStyleguide` | string | no | Reference styleguide id |
| `includeLinkedStyleguides` | boolean | no | Whether to include linked styleguides or not |
| `includeLatestVersion` | boolean | no | Whether to include the latest version data in the Component object |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": 1,
      "description": "string",
      "id": "string",
      "image": {},
      "name": "Ava Chen",
      "section": {},
      "source": {},
      "updated": 1,
      "variant_properties": [
        {}
      ]
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
| `image` | object |  |
| `name` | string |  |
| `section` | object |  |
| `source` | object |  |
| `updated` | number |  |
| `variant_properties` | array<object> |  |

## Native endpoint

Through the native Zeplin API, this operation is `GET /styleguides/{styleguide_id}/components` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-styleguide-components.md) for the provider-specific parameters and requirements.

