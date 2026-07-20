# Release0: Get Agent

Retrieves an agent from Release0.

```
GET https://connect.mindcloud.co/v1/universal/release0/latest/actions/get-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Release0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/release0/latest/actions/get-agent?connectionId=$CONNECTION_ID&agentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/release0/latest/actions/get-agent?${params}`, {
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
| `agentId` | string | yes | The agent ID. |

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
        "domainRef": "string",
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
| `tenancy.domainRef` | string |  |
| `tenancy.workspaceRef` | string |  |
| `timestamps.created` | string |  |
| `timestamps.updated` | string |  |

## Native endpoint

Through the native Release0 API, this operation is `GET /v1/agents/:agentId` (base URL `https://release0.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agent.md) for the provider-specific parameters and requirements.

