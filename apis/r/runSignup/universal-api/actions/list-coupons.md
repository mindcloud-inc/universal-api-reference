# RunSignup: List Coupons



```
GET https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/list-coupons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RunSignup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/list-coupons?connectionId=$CONNECTION_ID&raceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "raceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/list-coupons?${params}`, {
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
| `raceId` | string | yes | Path parameter: race_id |
| `page` | number | no | Page number to get. |
| `resultsPerPage` | number | no | Number of results per page. |
| `couponCode` | string | no | Search by coupon code. |
| `currentlyAvailableOnly` | string | no | Only include coupons that are currently available based on date. |
| `createdSince` | string | no | Searches for coupons created since the given date. |
| `createdOnOrBefore` | string | no | Searches for coupons created on or before the given date. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native RunSignup API returns.

## Native endpoint

Through the native RunSignup API, this operation is `GET /race/:race_id/coupons` (base URL `https://api.runsignup.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-coupons.md) for the provider-specific parameters and requirements.

