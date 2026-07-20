# Fiserv: List Payouts

Retrieves payouts for an account from Fiserv.

```
GET https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/list-payouts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiserv `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/list-payouts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/list-payouts?${params}`, {
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
| `limit` | number | no | Maximum number of payouts to return. |
| `status` | list | no | Payout status filter. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fiserv API returns.

## Native endpoint

Through the native Fiserv API, this operation is `GET /payouts` (base URL `https://bankinghub-cert.fiservapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-payouts.md) for the provider-specific parameters and requirements.

