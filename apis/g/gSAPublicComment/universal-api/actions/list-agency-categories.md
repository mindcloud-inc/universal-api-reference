# GSA Public Comment: List Agency Categories

Retrieves agency categories for an acronym from GSA Public Comment.

```
GET https://connect.mindcloud.co/v1/universal/gSAPublicComment/latest/actions/list-agency-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GSA Public Comment `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gSAPublicComment/latest/actions/list-agency-categories?connectionId=$CONNECTION_ID&acronym=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "acronym": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gSAPublicComment/latest/actions/list-agency-categories?${params}`, {
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
| `acronym` | string | yes | Agency acronym, such as FAA. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "attributes": {
            "acronym": "string",
            "category": "string",
            "default": true
          },
          "id": "string",
          "links": {
            "self": "https://example.com"
          },
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Agency category resources. |
| `data[].attributes.acronym` | string |  |
| `data[].attributes.category` | string |  |
| `data[].attributes.default` | boolean |  |
| `data[].id` | string |  |
| `data[].links.self` | string |  |
| `data[].type` | string |  |

## Native endpoint

Through the native GSA Public Comment API, this operation is `GET /agency-categories` (base URL `https://api.regulations.gov/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-agency-categories.md) for the provider-specific parameters and requirements.

