# Particle: Delete Ledger Instance



```
DELETE https://connect.mindcloud.co/v1/universal/particle/latest/actions/delete-ledger-instance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Particle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/particle/latest/actions/delete-ledger-instance?connectionId=$CONNECTION_ID&ledgerName=Ava%20Chen&scopeValue=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ledgerName": "Ava Chen",
  "scopeValue": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/particle/latest/actions/delete-ledger-instance?${params}`, {
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
| `ledgerName` | string | yes |  |
| `scopeValue` | string | yes |  |

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

Through the native Particle API, this operation is `DELETE /v1/ledgers/:ledgerName/instances/:scopeValue` (base URL `https://api.particle.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-ledger-instance.md) for the provider-specific parameters and requirements.

