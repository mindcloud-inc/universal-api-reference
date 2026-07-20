# Shuffll: Create Project

Creates a new project in Shuffll.

```
POST https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shuffll `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "prompt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `language` | string | no | Optional output language. |
| `prompt` | string | yes | Project creation prompt. |
| `promptType` | string | no | Optional prompt type. |
| `toAutoEnhance` | string | no | Whether to auto enhance after project creation. |
| `toAutoExport` | string | no | Whether to auto export after project creation. |
| `videoLength` | string | no | Optional target video length in seconds. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "projectId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `projectId` | string | Created project id. |

## Native endpoint

Through the native Shuffll API, this operation is `POST /auth/project/create` (base URL `https://api.shuffll.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

