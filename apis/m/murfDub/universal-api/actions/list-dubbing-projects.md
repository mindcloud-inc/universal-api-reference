# Murf Dub: List Dubbing Projects

Retrieves dubbing projects from Murf Dub.

```
GET https://connect.mindcloud.co/v1/universal/murfDub/latest/actions/list-dubbing-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Murf Dub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/murfDub/latest/actions/list-dubbing-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/murfDub/latest/actions/list-dubbing-projects?${params}`, {
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
| `limit` | number | no | Number of projects to return. |
| `next` | string | no | Next page iterator returned by the previous response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "next": "string",
      "projects": [
        {
          "description": "string",
          "dubbing_type": "string",
          "name": "Ava Chen",
          "project_id": "string",
          "source_locale": "string",
          "target_locales": [
            "string"
          ]
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
| `next` | string |  |
| `projects[].description` | string |  |
| `projects[].dubbing_type` | string |  |
| `projects[].name` | string |  |
| `projects[].project_id` | string |  |
| `projects[].source_locale` | string |  |
| `projects[].target_locales` | array<string> |  |

## Native endpoint

Through the native Murf Dub API, this operation is `GET /v1/murfdub/projects/list` (base URL `https://api.murf.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-dubbing-projects.md) for the provider-specific parameters and requirements.

