# Morningmate: Create Project

Creates a new project in Morningmate.

```
POST https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Morningmate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "registerId": "apps@mindcloud.co",
  "title": "Codex Morningmate Test Project"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "registerId": "apps@mindcloud.co",
    "title": "Codex Morningmate Test Project"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `registerId` | string | yes | Morningmate author user ID Example: `apps@mindcloud.co`. |
| `title` | string | yes | Project title Example: `Codex Morningmate Test Project`. |
| `description` | string | no | Project description Example: `Created by Codex during Morningmate app verification.`. |

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
| `projectId` | string |  |

## Native endpoint

Through the native Morningmate API, this operation is `POST /v1/projects` (base URL `https://api.morningmate.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

