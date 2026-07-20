# smsmode: Lookup Number



```
GET https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/lookup-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a smsmode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/lookup-number?connectionId=$CONNECTION_ID&msisdn=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "msisdn": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/lookup-number?${params}`, {
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
| `msisdn` | string | yes | MSISDN path parameter from the smsmode API route. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string",
      "countryPrefix": "string",
      "isoCountryCode": "string",
      "mcc": "string",
      "mccMnc": "string",
      "mnc": "string",
      "network": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string |  |
| `countryPrefix` | string |  |
| `isoCountryCode` | string |  |
| `mcc` | string |  |
| `mccMnc` | string |  |
| `mnc` | string |  |
| `network` | string |  |

## Native endpoint

Through the native smsmode API, this operation is `GET commons/v1/lookup/:msisdn` (base URL `https://rest.smsmode.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-number.md) for the provider-specific parameters and requirements.

