# Routee: Get pricing for all Routee Services

Retrieves pricing for all Routee services.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/get-pricing-for-all-routee-services
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/get-pricing-for-all-routee-services?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/get-pricing-for-all-routee-services?${params}`, {
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
| `mcc` | string | no | The mcc to filter price results. |
| `mnc` | string | no | The mnc to filter price results. |
| `service` | string | no | The service to filter price results (possible values: Sms, Voice, TwoStep, Lookup, NumberValidator, Viber). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currency": {
        "code": "string",
        "name": "Ava Chen",
        "sign": "string"
      },
      "lookup": {
        "perRequest": 1
      },
      "numberValidator": {
        "withoutPortedInfo": 1,
        "withPortedInfo": 1
      },
      "sms": [
        [
          {}
        ]
      ],
      "twoStep": {
        "sms": 1,
        "voice": 1
      },
      "viber": [
        [
          {}
        ]
      ],
      "voice": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | object |  |
| `currency.code` | string |  |
| `currency.name` | string |  |
| `currency.sign` | string |  |
| `lookup` | object |  |
| `lookup.perRequest` | number |  |
| `numberValidator` | object |  |
| `numberValidator.withoutPortedInfo` | number |  |
| `numberValidator.withPortedInfo` | number |  |
| `sms[]` | array<object> |  |
| `sms[].country` | string |  |
| `sms[].iso` | string |  |
| `sms[].mcc` | string |  |
| `sms[].networks[]` | array<object> |  |
| `sms[].networks[].mnc` | string |  |
| `sms[].networks[].network` | string |  |
| `sms[].networks[].price` | number |  |
| `twoStep` | object |  |
| `twoStep.sms` | number |  |
| `twoStep.voice` | number |  |
| `viber[]` | array<object> |  |
| `viber[].country` | string |  |
| `viber[].iso` | string |  |
| `viber[].prices` | object |  |
| `viber[].prices.fee` | string |  |
| `viber[].prices.feePeriod` | string |  |
| `viber[].prices.promotionalInbound` | string |  |
| `viber[].prices.promotionalOutbound` | string |  |
| `viber[].prices.transactionalInbound` | string |  |
| `viber[].prices.transactionalOutbound` | string |  |
| `voice[]` | array<object> |  |
| `voice[].country` | string |  |
| `voice[].iso` | string |  |
| `voice[].landlinePrice` | string |  |
| `voice[].mobilePrice` | string |  |

## Native endpoint

Through the native Routee API, this operation is `GET /system/prices` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pricing-for-all-routee-services.md) for the provider-specific parameters and requirements.

