# Lookify: Lookup Carrier



```
GET https://connect.mindcloud.co/v1/universal/lookify/latest/actions/lookup-carrier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lookify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lookify/latest/actions/lookup-carrier?connectionId=$CONNECTION_ID&nid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "nid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lookify/latest/actions/lookup-carrier?${params}`, {
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
| `nid` | string | yes | The phone number to search. |
| `country` | string | no | Optional country for the phone number search. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billingPeriod": "string",
      "billingPeriodUsage": 1,
      "carrier": "string",
      "country": "string",
      "nid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingPeriod` | string | Billing period for the request usage, formatted as YYYY-MM. |
| `billingPeriodUsage` | number | Count of successful carrier lookups recorded for the billing period. |
| `carrier` | string | Carrier name returned for the phone number. |
| `country` | string | Country associated with the lookup result. |
| `nid` | string | Phone number identifier returned by Lookify. |

## Native endpoint

Through the native Lookify API, this operation is `POST /api/enterprise/carrier` (base URL `https://lookify.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-carrier.md) for the provider-specific parameters and requirements.

