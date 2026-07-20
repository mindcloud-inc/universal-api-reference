# PhantomBuster: List Containers

Retrieves containers from PhantomBuster.

```
GET https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/list-containers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PhantomBuster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/list-containers?connectionId=$CONNECTION_ID&agentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/list-containers?${params}`, {
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
| `agentId` | string | yes | Id of the agent to fetch containers from. |
| `beforeEndedAt` | string | no |  |
| `mode` | list | no | One of: `all`, `finalized`. |
| `withRuntimeEvents` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "containers": [
        {}
      ],
      "maxLimitReached": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `containers` | array<object> |  |
| `maxLimitReached` | boolean |  |

## Native endpoint

Through the native PhantomBuster API, this operation is `GET /containers/fetch-all` (base URL `https://api.phantombuster.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-containers.md) for the provider-specific parameters and requirements.

