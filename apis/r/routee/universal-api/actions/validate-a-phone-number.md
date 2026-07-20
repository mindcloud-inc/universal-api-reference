# Routee: Validate a phone number

Validates a phone number in Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/validate-a-phone-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/validate-a-phone-number?connectionId=$CONNECTION_ID&to=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "to": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/validate-a-phone-number?${params}`, {
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
| `getPorted` | boolean | no | Indicates if the number validator result will concern the number's ported network (only if the number is ported). Pricing differs if you select this option. Visit [here](https://dev.routee.net/#/management/financial/pricing) for pricing information. Default value: false |
| `to` | string | yes | The number that the number validator service will use. Format with a '+' and country code (E.164 format). |
| `host` | string | no | The host name or the IP address. This field is used in order to get information about the country of an IP or a domain name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applicationName": "Ava Chen",
      "createdAt": "string",
      "details": {
        "countryCode": "string",
        "countryPrefix": "string",
        "network": "string",
        "networkCode": "string",
        "ported": true,
        "type": "string"
      },
      "formats": {
        "international": "string",
        "national": "string",
        "rfc3966": "string"
      },
      "geo": {
        "continent": "string",
        "country": "string",
        "countryISO2Code": "string",
        "countryISO3Code": "string",
        "host": "string"
      },
      "getPorted": true,
      "numberValidatorId": "string",
      "to": "string",
      "valid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applicationName` | string |  |
| `createdAt` | string |  |
| `details` | object |  |
| `details.countryCode` | string |  |
| `details.countryPrefix` | string |  |
| `details.network` | string |  |
| `details.networkCode` | string |  |
| `details.ported` | boolean |  |
| `details.type` | string |  |
| `formats` | object |  |
| `formats.international` | string |  |
| `formats.national` | string |  |
| `formats.rfc3966` | string |  |
| `geo` | object |  |
| `geo.continent` | string |  |
| `geo.country` | string |  |
| `geo.countryISO2Code` | string |  |
| `geo.countryISO3Code` | string |  |
| `geo.host` | string |  |
| `getPorted` | boolean |  |
| `numberValidatorId` | string |  |
| `to` | string |  |
| `valid` | boolean |  |

## Native endpoint

Through the native Routee API, this operation is `POST /numbervalidator` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-a-phone-number.md) for the provider-specific parameters and requirements.

