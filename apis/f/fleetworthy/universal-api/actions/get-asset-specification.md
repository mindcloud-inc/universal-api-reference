# Fleetworthy: Get Asset Specification



```
GET https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/get-asset-specification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetworthy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/get-asset-specification?connectionId=$CONNECTION_ID&assetSpecificationId=550e8400-e29b-41d4-a716-446655440000" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "assetSpecificationId": "550e8400-e29b-41d4-a716-446655440000"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/get-asset-specification?${params}`, {
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
| `assetSpecificationId` | string | yes | The unique identifier of the asset specification. Example: `550e8400-e29b-41d4-a716-446655440000`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fleetworthy API returns.

## Native endpoint

Through the native Fleetworthy API, this operation is `GET /asset-specifications/:assetSpecificationId` (base URL `https://apis.fleetworthy.com/compliance-api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-asset-specification.md) for the provider-specific parameters and requirements.

