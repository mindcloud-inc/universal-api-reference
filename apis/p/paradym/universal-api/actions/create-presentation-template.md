# Paradym: Create Presentation Template

Creates a presentation template in Paradym.

```
POST https://connect.mindcloud.co/v1/universal/paradym/latest/actions/create-presentation-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paradym `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/paradym/latest/actions/create-presentation-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "credentials[0].type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paradym/latest/actions/create-presentation-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "credentials[0].type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `description` | string | no |  |
| `credentials[0].type` | string | yes | The SD-JWT VC type to request in the presentation template. |
| `credentials[0].name` | string | no | Label for the requested credential in the template. Default: `MindCloud Test Credential Request`. |
| `credentials[0].description` | string | no | Description for the requested credential in the template. Default: `Request the test subject full name`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Paradym API returns.

## Native endpoint

Through the native Paradym API, this operation is `POST /projects/:projectId/templates/presentations` (base URL `https://api.paradym.id/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-presentation-template.md) for the provider-specific parameters and requirements.

