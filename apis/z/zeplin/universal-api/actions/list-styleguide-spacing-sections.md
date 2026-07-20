# Zeplin: List Styleguide Spacing Sections

Retrieves a list of styleguide spacing sections from Zeplin.

```
GET https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-styleguide-spacing-sections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-styleguide-spacing-sections?connectionId=$CONNECTION_ID&limit=25&offset=0&styleguideId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "styleguideId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-styleguide-spacing-sections?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "base_token": {},
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `base_token` | object |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Zeplin API, this operation is `GET /styleguides/{styleguide_id}/spacing_sections` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-styleguide-spacing-sections.md) for the provider-specific parameters and requirements.

