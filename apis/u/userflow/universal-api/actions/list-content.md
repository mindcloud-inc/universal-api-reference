# Userflow: List Content

Retrieves a list of content objects from Userflow.

```
GET https://connect.mindcloud.co/v1/universal/userflow/latest/actions/list-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Userflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/userflow/latest/actions/list-content?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/userflow/latest/actions/list-content?${params}`, {
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
| `limit` | number | no | Maximum number of content objects to return. |
| `orderBy` | string | no | Sort content objects by created_at or name. |
| `startingAfter` | string | no | Return content objects after this content ID. |
| `type` | string | no | Filter content by type: checklist, flow, or launcher. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "created_at": "2026-05-07T12:00:00.000Z",
          "draft_version": {},
          "draft_version_id": "string",
          "id": "string",
          "name": "Ava Chen",
          "object": "string",
          "published_version": {},
          "published_version_id": "string",
          "type": "string"
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
| `data` | array<object> | List of content objects. |
| `data[].created_at` | date | Content creation timestamp. |
| `data[].draft_version` | object | Draft version object. |
| `data[].draft_version_id` | string | Draft version ID. |
| `data[].id` | string | Content ID. |
| `data[].name` | string | Content name. |
| `data[].object` | string | Returned object type. |
| `data[].published_version` | object | Published version object. |
| `data[].published_version_id` | string | Published version ID. |
| `data[].type` | string | Content type. |
| `has_more` | boolean | Whether more results are available. |
| `next_page_url` | string | URL for the next page. |
| `object` | string | Response object type. |
| `url` | string | Current page URL. |

## Native endpoint

Through the native Userflow API, this operation is `GET /content` (base URL `https://api.userflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-content.md) for the provider-specific parameters and requirements.

