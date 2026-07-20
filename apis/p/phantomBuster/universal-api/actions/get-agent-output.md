# PhantomBuster: Get Agent Output

Retrieves agent output from PhantomBuster.

```
GET https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/get-agent-output
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PhantomBuster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/get-agent-output?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/get-agent-output?${params}`, {
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
| `fromOutputPos` | number | no |  |
| `id` | string | yes | The PhantomBuster agent ID whose latest output you want. |
| `prevContainerId` | string | no |  |
| `prevRuntimeEventIndex` | number | no |  |
| `prevStatus` | list | no | One of: `finished`, `launch error`, `never launched`, `running`, `starting`, `unknown`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canSoftAbort": true,
      "isAgentRunning": true,
      "outputPos": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canSoftAbort` | boolean |  |
| `isAgentRunning` | boolean |  |
| `outputPos` | number |  |
| `status` | string |  |

## Native endpoint

Through the native PhantomBuster API, this operation is `GET /agents/fetch-output` (base URL `https://api.phantombuster.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agent-output.md) for the provider-specific parameters and requirements.

