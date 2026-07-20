# Restream: Get Clip Project

Retrieves a clip project from Restream by ID.

```
GET https://connect.mindcloud.co/v1/universal/restream/latest/actions/get-clip-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Restream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/restream/latest/actions/get-clip-project?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/restream/latest/actions/get-clip-project?${params}`, {
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
| `projectId` | string | yes | The ID of the clip project to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clips": [
        {}
      ],
      "generatingClipsNow": true,
      "postedClips": [
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
| `clips` | array<object> |  |
| `generatingClipsNow` | boolean |  |
| `postedClips` | array<object> |  |

## Native endpoint

Through the native Restream API, this operation is `GET /user/clips/projects/:projectId` (base URL `https://api.restream.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-clip-project.md) for the provider-specific parameters and requirements.

