# Calibre: Create Deploy

Creates a new deploy in Calibre.

```
POST https://connect.mindcloud.co/v1/universal/calibre/latest/actions/create-deploy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calibre `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/calibre/latest/actions/create-deploy" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.site": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/calibre/latest/actions/create-deploy', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.site": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.site` | string | yes | Site slug, found in site settings. |
| `variables.revision` | string | no | Source control revision or tag name for the deploy. |
| `variables.repository` | string | no | Base URL of the repository containing the deployed code. |
| `variables.username` | string | no | Name of the user who deployed the code. |
| `variables.createdAt` | string | no | ISO8601 timestamp for when the deploy was created. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createDeploy": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "repository": "string",
        "revision": "string",
        "url": "https://example.com",
        "username": "Ava Chen",
        "uuid": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createDeploy.createdAt` | date |  |
| `createDeploy.repository` | string |  |
| `createDeploy.revision` | string |  |
| `createDeploy.url` | string |  |
| `createDeploy.username` | string |  |
| `createDeploy.uuid` | string |  |

## Native endpoint

Through the native Calibre API, this operation is `POST /graphql` (base URL `https://api.calibreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-deploy.md) for the provider-specific parameters and requirements.

