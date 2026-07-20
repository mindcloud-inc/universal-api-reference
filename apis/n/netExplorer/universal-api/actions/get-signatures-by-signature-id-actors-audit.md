# NetExplorer: Get Audit



```
GET https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-signatures-by-signature-id-actors-audit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-signatures-by-signature-id-actors-audit?connectionId=$CONNECTION_ID&signatureId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "signatureId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-signatures-by-signature-id-actors-audit?${params}`, {
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
| `signatureId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native NetExplorer API returns.

## Native endpoint

Through the native NetExplorer API, this operation is `GET /signatures/:signatureId/actors/audit` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-signatures-by-signature-id-actors-audit.md) for the provider-specific parameters and requirements.

