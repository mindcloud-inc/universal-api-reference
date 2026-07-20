# Particle: Delete Logic Function



```
DELETE https://connect.mindcloud.co/v1/universal/particle/latest/actions/delete-logic-function
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Particle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/particle/latest/actions/delete-logic-function?connectionId=$CONNECTION_ID&logicFunctionId=00000000-0000-0000-0000-000000000000" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "logicFunctionId": "00000000-0000-0000-0000-000000000000"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/particle/latest/actions/delete-logic-function?${params}`, {
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
| `logicFunctionId` | string | yes | Default: `00000000-0000-0000-0000-000000000000`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ok` | boolean |  |

## Native endpoint

Through the native Particle API, this operation is `DELETE /v1/logic/functions/:logicFunctionId` (base URL `https://api.particle.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-logic-function.md) for the provider-specific parameters and requirements.

