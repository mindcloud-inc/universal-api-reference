# Viqeo: Get Story

Retrieves a story record from Viqeo.

```
GET https://connect.mindcloud.co/v1/universal/viqeo/latest/actions/get-story
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viqeo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/viqeo/latest/actions/get-story?connectionId=$CONNECTION_ID&projectId=string&storyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "storyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/viqeo/latest/actions/get-story?${params}`, {
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
| `projectId` | string | yes | Project identifier from the path. |
| `storyId` | string | yes | Story identifier from the path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Story identifier. |
| `title` | string | Story title. |

## Native endpoint

Through the native Viqeo API, this operation is `GET /media-platform/v1/project/:projectId/story/:storyId` (base URL `https://api.viqeo.tv`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-story.md) for the provider-specific parameters and requirements.

