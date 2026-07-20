# Iris Dfir: Delete Asset



```
DELETE https://connect.mindcloud.co/v1/universal/irisDfir/latest/actions/delete-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Iris Dfir `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/irisDfir/latest/actions/delete-asset?connectionId=$CONNECTION_ID&caseIdentifier=1&identifier=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "caseIdentifier": "1",
  "identifier": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/irisDfir/latest/actions/delete-asset?${params}`, {
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
| `caseIdentifier` | number | yes | IRIS case identifier. |
| `identifier` | number | yes | IRIS asset identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Iris Dfir API returns.

## Native endpoint

Through the native Iris Dfir API, this operation is `DELETE /api/v2/cases/:case_identifier/assets/:identifier` (base URL `https://v200.beta.dfir-iris.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-asset.md) for the provider-specific parameters and requirements.

