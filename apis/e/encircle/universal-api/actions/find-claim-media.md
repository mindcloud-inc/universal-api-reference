# Encircle: Find Claim Media

Retrieves claim media from Encircle.

```
GET https://connect.mindcloud.co/v1/universal/encircle/latest/actions/find-claim-media
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encircle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encircle/latest/actions/find-claim-media?connectionId=$CONNECTION_ID&propertyClaimId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "propertyClaimId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encircle/latest/actions/find-claim-media?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no |  |
| `after` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Encircle API returns.

## Native endpoint

Through the native Encircle API, this operation is `GET /v1/property_claims/:property_claim_id/media` (base URL `https://api.encircleapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-claim-media.md) for the provider-specific parameters and requirements.

