# Userflow: List Attribute Definitions

Retrieves a list of attribute definitions from Userflow.

```
GET https://connect.mindcloud.co/v1/universal/userflow/latest/actions/list-attribute-definitions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Userflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/userflow/latest/actions/list-attribute-definitions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/userflow/latest/actions/list-attribute-definitions?${params}`, {
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
| `limit` | number | no | Maximum number of attribute definitions to return. |
| `orderBy` | string | no | Sort attribute definitions by created_at, display_name, or name. |
| `scope` | string | no | Filter attribute definitions by scope. |
| `startingAfter` | string | no | Return attribute definitions after this definition ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "created_at": "2026-05-07T12:00:00.000Z",
          "data_type": "string",
          "description": "string",
          "display_name": "Ava Chen",
          "id": "string",
          "name": "Ava Chen",
          "object": "string",
          "scope": "string"
        }
      ],
      "has_more": true,
      "next_page_url": "https://example.com",
      "object": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | List of attribute definitions. |
| `data[].created_at` | date | Definition creation timestamp. |
| `data[].data_type` | string | Attribute data type. |
| `data[].description` | string | Definition description. |
| `data[].display_name` | string | Display name. |
| `data[].id` | string | Attribute definition ID. |
| `data[].name` | string | Internal name. |
| `data[].object` | string | Returned object type. |
| `data[].scope` | string | Definition scope. |
| `has_more` | boolean | Whether more results are available. |
| `next_page_url` | string | URL for the next page. |
| `object` | string | Response object type. |
| `url` | string | Current page URL. |

## Native endpoint

Through the native Userflow API, this operation is `GET /attribute_definitions` (base URL `https://api.userflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-attribute-definitions.md) for the provider-specific parameters and requirements.

