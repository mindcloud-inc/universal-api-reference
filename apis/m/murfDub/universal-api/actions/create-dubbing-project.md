# Murf Dub: Create Dubbing Project

Creates a dubbing project in Murf Dub.

```
POST https://connect.mindcloud.co/v1/universal/murfDub/latest/actions/create-dubbing-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Murf Dub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/murfDub/latest/actions/create-dubbing-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "dubbingType": "string",
  "targetLocales[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/murfDub/latest/actions/create-dubbing-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "dubbingType": "string",
    "targetLocales[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Project name. |
| `dubbingType` | string | yes | Dubbing workflow type. |
| `targetLocales[]` | array<string> | yes | Locales to generate in the project. |
| `sourceLocale` | string | no | Source language locale for the project. |
| `description` | string | no | Project description. |

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

Through the native Murf Dub API, this operation is `POST /v1/murfdub/projects/create` (base URL `https://api.murf.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-dubbing-project.md) for the provider-specific parameters and requirements.

