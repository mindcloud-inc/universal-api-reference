# Userflow: Get Content

Retrieves a content object from Userflow by ID.

```
GET https://connect.mindcloud.co/v1/universal/userflow/latest/actions/get-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Userflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/userflow/latest/actions/get-content?connectionId=$CONNECTION_ID&contentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/userflow/latest/actions/get-content?${params}`, {
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
| `contentId` | string | yes | Unique identifier for the content object. |

## Response

```json
{
  "success": true,
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
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | Content creation timestamp. |
| `draft_version` | object | Draft version object. |
| `draft_version_id` | string | Draft version ID. |
| `id` | string | Content ID. |
| `name` | string | Content name. |
| `object` | string | Returned object type. |
| `published_version` | object | Published version object. |
| `published_version_id` | string | Published version ID. |
| `type` | string | Content type. |

## Native endpoint

Through the native Userflow API, this operation is `GET /content/:content_id` (base URL `https://api.userflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-content.md) for the provider-specific parameters and requirements.

