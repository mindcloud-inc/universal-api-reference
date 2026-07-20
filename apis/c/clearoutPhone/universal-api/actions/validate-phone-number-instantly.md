# ClearoutPhone: Validate Phone Number Instantly

Retrieves instant validation details for a phone number from ClearoutPhone.

```
GET https://connect.mindcloud.co/v1/universal/clearoutPhone/latest/actions/validate-phone-number-instantly
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClearoutPhone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clearoutPhone/latest/actions/validate-phone-number-instantly?connectionId=$CONNECTION_ID&number=7766733573" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "number": "7766733573"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clearoutPhone/latest/actions/validate-phone-number-instantly?${params}`, {
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
| `number` | string | yes | A phone number to validate Example: `7766733573`. |
| `countryCode` | string | no | Country code of phone number to be validated Example: `GB`. |
| `timeout` | number | no | Request wait time in milliseconds Default: `5000`. Example: `5000`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billableCredits": 1,
      "canBeInternationallyDialled": "string",
      "carrier": "string",
      "countryCode": "string",
      "countryDstobservedhrs": 1,
      "countryName": "Ava Chen",
      "countryTimezone": "string",
      "countryUtcoffset": "string",
      "e164Format": "string",
      "internationalFormat": "string",
      "lineType": "string",
      "localFormat": "string",
      "location": "string",
      "status": "string",
      "timeTaken": 1,
      "validatedOn": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billableCredits` | number |  |
| `canBeInternationallyDialled` | string |  |
| `carrier` | string |  |
| `countryCode` | string |  |
| `countryDstobservedhrs` | number |  |
| `countryName` | string |  |
| `countryTimezone` | string |  |
| `countryUtcoffset` | string |  |
| `e164Format` | string |  |
| `internationalFormat` | string |  |
| `lineType` | string |  |
| `localFormat` | string |  |
| `location` | string |  |
| `status` | string |  |
| `timeTaken` | number |  |
| `validatedOn` | date |  |

## Native endpoint

Through the native ClearoutPhone API, this operation is `POST /phonenumber/validate` (base URL `https://api.clearoutphone.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-phone-number-instantly.md) for the provider-specific parameters and requirements.

