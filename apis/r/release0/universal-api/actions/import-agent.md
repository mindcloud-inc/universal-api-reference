# Release0: Import Agent

Imports an agent into Release0.

```
POST https://connect.mindcloud.co/v1/universal/release0/latest/actions/import-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Release0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/release0/latest/actions/import-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "agent": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/release0/latest/actions/import-agent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "agent": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | string | yes | The workspace that will receive the imported agent. |
| `agent` | object | yes | The full agent definition to import. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "exposure": {
        "access": {
          "url": "https://example.com"
        },
        "state": {
          "archived": true,
          "locked": true,
          "published": true
        }
      },
      "profile": {
        "title": "string"
      },
      "ref": {
        "key": "string",
        "publicKey": "string",
        "revision": "string"
      },
      "tenancy": {
        "domainRef": "string",
        "workspaceRef": "string"
      },
      "timestamps": {
        "created": "2026-05-07T12:00:00.000Z",
        "updated": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `exposure.access.url` | string |  |
| `exposure.state.archived` | boolean |  |
| `exposure.state.locked` | boolean |  |
| `exposure.state.published` | boolean |  |
| `profile.title` | string |  |
| `ref.key` | string |  |
| `ref.publicKey` | string |  |
| `ref.revision` | string |  |
| `tenancy.domainRef` | string |  |
| `tenancy.workspaceRef` | string |  |
| `timestamps.created` | date |  |
| `timestamps.updated` | date |  |

## Native endpoint

Through the native Release0 API, this operation is `POST /v1/agents/import` (base URL `https://release0.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-agent.md) for the provider-specific parameters and requirements.

