# Encircle: Find Claim Rooms

Retrieves claim rooms from Encircle.

```
GET https://connect.mindcloud.co/v1/universal/encircle/latest/actions/find-claim-rooms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encircle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encircle/latest/actions/find-claim-rooms?connectionId=$CONNECTION_ID&propertyClaimId=1&structureId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "propertyClaimId": "1",
  "structureId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encircle/latest/actions/find-claim-rooms?${params}`, {
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
| `propertyClaimId` | number | yes |  |
| `structureId` | number | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `order` | list | no | One of: `newest`, `oldest`. |
| `limit` | number | no |  |
| `after` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Encircle API returns.

## Native endpoint

Through the native Encircle API, this operation is `GET /v1/property_claims/:property_claim_id/structures/:structure_id/rooms` (base URL `https://api.encircleapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-claim-rooms.md) for the provider-specific parameters and requirements.

