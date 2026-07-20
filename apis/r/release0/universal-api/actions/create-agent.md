# Release0: Create Agent

Creates a new agent in Release0.

```
POST https://connect.mindcloud.co/v1/universal/release0/latest/actions/create-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Release0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/release0/latest/actions/create-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/release0/latest/actions/create-agent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agent` | object | no | Optional agent payload object for draft creation. |
| `workspaceId` | string | yes | The workspace ID that will own the new agent. |

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
        "workspaceRef": "string"
      },
      "timestamps": {
        "created": "string",
        "updated": "string"
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
| `exposure.state.published` | boolean |  |
| `profile.title` | string |  |
| `ref.key` | string |  |
| `ref.publicKey` | string |  |
| `ref.revision` | string |  |
| `tenancy.workspaceRef` | string |  |
| `timestamps.created` | string |  |
| `timestamps.updated` | string |  |

## Native endpoint

Through the native Release0 API, this operation is `POST /v1/agents` (base URL `https://release0.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-agent.md) for the provider-specific parameters and requirements.

