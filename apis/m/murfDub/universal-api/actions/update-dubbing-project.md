# Murf Dub: Update Dubbing Project

Updates a dubbing project in Murf Dub.

```
PUT https://connect.mindcloud.co/v1/universal/murfDub/latest/actions/update-dubbing-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Murf Dub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/murfDub/latest/actions/update-dubbing-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "targetLocales[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/murfDub/latest/actions/update-dubbing-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "targetLocales[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | The Murf Dub project ID to update. |
| `targetLocales[]` | array<string> | yes | Locales to keep on the project. |

## Response

```json
{
  "success": true,
  "data": [
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `dubbing_type` | string |  |
| `name` | string |  |
| `project_id` | string |  |
| `source_locale` | string |  |
| `target_locales` | array<string> |  |

## Native endpoint

Through the native Murf Dub API, this operation is `PUT /v1/murfdub/projects/:project_id/update` (base URL `https://api.murf.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-dubbing-project.md) for the provider-specific parameters and requirements.

