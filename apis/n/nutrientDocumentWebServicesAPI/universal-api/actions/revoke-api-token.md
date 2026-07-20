# Nutrient Document Web Services: Revoke API Token

Deletes an API token from Nutrient Document Web Services API.

```
DELETE https://connect.mindcloud.co/v1/universal/nutrientDocumentWebServicesAPI/latest/actions/revoke-api-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nutrient Document Web Services `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/nutrientDocumentWebServicesAPI/latest/actions/revoke-api-token?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nutrientDocumentWebServicesAPI/latest/actions/revoke-api-token?${params}`, {
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
| `id` | string | yes | Token identifier to revoke. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Nutrient Document Web Services API returns.

## Native endpoint

Through the native Nutrient Document Web Services API, this operation is `DELETE /tokens` (base URL `https://api.nutrient.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/revoke-api-token.md) for the provider-specific parameters and requirements.

