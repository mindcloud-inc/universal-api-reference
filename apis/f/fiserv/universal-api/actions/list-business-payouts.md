# Fiserv: List Business Payouts

Retrieves payouts for a business from Fiserv.

```
GET https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/list-business-payouts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiserv `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/list-business-payouts?connectionId=$CONNECTION_ID&xBusinessId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "xBusinessId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/list-business-payouts?${params}`, {
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
| `endingBefore` | string | no | Cursor ID to end before. |
| `startingAfter` | string | no | Cursor ID to start after. |
| `xBusinessId` | string | yes | Business ID required in the x-business-id header. |
| `limit` | number | no | Maximum number of business payouts to return. Official max is 50. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fiserv API returns.

## Native endpoint

Through the native Fiserv API, this operation is `GET /businesses/payouts` (base URL `https://bankinghub-cert.fiservapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-business-payouts.md) for the provider-specific parameters and requirements.

