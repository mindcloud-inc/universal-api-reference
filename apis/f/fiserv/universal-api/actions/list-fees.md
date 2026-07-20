# Fiserv: List Fees

Retrieves fees for a merchant account from Fiserv.

```
GET https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/list-fees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiserv `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/list-fees?connectionId=$CONNECTION_ID&xAccountId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "xAccountId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/list-fees?${params}`, {
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
| `sourceId` | string | no | Filter fees by source ID. |
| `startingAfter` | string | no | Cursor ID to start after. |
| `xAccountId` | string | yes | Merchant account ID required in the x-account-id header. |
| `limit` | number | no | Maximum number of fees to return. |
| `feeType` | list | no | Filter by fee type. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fiserv API returns.

## Native endpoint

Through the native Fiserv API, this operation is `GET /fees` (base URL `https://bankinghub-cert.fiservapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-fees.md) for the provider-specific parameters and requirements.

