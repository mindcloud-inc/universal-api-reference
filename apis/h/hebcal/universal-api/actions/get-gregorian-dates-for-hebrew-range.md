# Hebcal: Get Gregorian Dates for Hebrew Range

Retrieves Gregorian dates for a Hebrew date range in Hebcal.

```
GET https://connect.mindcloud.co/v1/universal/hebcal/latest/actions/get-gregorian-dates-for-hebrew-range
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hebcal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hebcal/latest/actions/get-gregorian-dates-for-hebrew-range?connectionId=$CONNECTION_ID&hy=string&hm=string&hd=string&ndays=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "hy": "string",
  "hm": "string",
  "hd": "string",
  "ndays": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hebcal/latest/actions/get-gregorian-dates-for-hebrew-range?${params}`, {
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
| `hy` | string | yes | Hebrew year. |
| `hm` | string | yes | Hebrew month name. |
| `hd` | string | yes | Hebrew day of month. |
| `ndays` | string | yes | Number of days to calculate. |
| `strict` | string | no | Return an error for invalid dates when enabled. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Hebcal API returns.

## Native endpoint

Through the native Hebcal API, this operation is `GET /converter` (base URL `https://www.hebcal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-gregorian-dates-for-hebrew-range.md) for the provider-specific parameters and requirements.

