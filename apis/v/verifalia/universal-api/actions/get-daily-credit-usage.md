# Verifalia: Get Daily Credit Usage

Retrieves daily credit usage from Verifalia.

```
GET https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/get-daily-credit-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verifalia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/get-daily-credit-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/get-daily-credit-usage?${params}`, {
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
| `date` | string | no | Get credit usage for one specific date in YYYY-MM-DD format. |
| `dateSince` | string | no | Inclusive start date for the credit-usage period in YYYY-MM-DD format. |
| `dateUntil` | string | no | Inclusive end date for the credit-usage period in YYYY-MM-DD format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditPacks": 1,
      "date": "string",
      "freeCredits": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditPacks` | number | Credits consumed from purchased credit packs on that date. |
| `date` | string | The usage date in YYYY-MM-DD format. |
| `freeCredits` | number | Free daily credits consumed on that date. |

## Native endpoint

Through the native Verifalia API, this operation is `GET /credits/daily-usage` (base URL `https://api-1.verifalia.com/v2.7`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-daily-credit-usage.md) for the provider-specific parameters and requirements.

