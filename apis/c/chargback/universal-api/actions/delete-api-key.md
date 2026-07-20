# Chargback: Delete API Key

Deletes an existing API key from Chargback.

```
DELETE https://connect.mindcloud.co/v1/universal/chargback/latest/actions/delete-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chargback `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/chargback/latest/actions/delete-api-key?connectionId=$CONNECTION_ID&platform=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "platform": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargback/latest/actions/delete-api-key?${params}`, {
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
| `platform` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Chargback API returns.

## Native endpoint

Through the native Chargback API, this operation is `DELETE /api/public/v1/api-keys/delete/` (base URL `https://api.chargeback.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-api-key.md) for the provider-specific parameters and requirements.

