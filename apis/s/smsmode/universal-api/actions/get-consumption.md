# smsmode: Get Consumption



```
GET https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/get-consumption
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a smsmode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/get-consumption?connectionId=$CONNECTION_ID&channelId=string&consumptionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelId": "string",
  "consumptionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/get-consumption?${params}`, {
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
| `channelId` | string | yes | Channel ID path parameter from the smsmode API route. |
| `consumptionId` | string | yes | Consumption ID path parameter from the smsmode API route. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel": {
        "channelId": "string",
        "flow": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "consumptionId": "string",
      "href": "string",
      "items": [
        {
          "lookup": {
            "country": "string",
            "countryPrefix": "string",
            "isoCountryCode": "string",
            "mcc": "string",
            "mccMnc": "string",
            "mnc": "string",
            "network": "string"
          },
          "price": {
            "amount": 1,
            "currency": "string"
          },
          "quantity": 1,
          "statuses": [
            {
              "quantity": 1,
              "value": "string"
            }
          ]
        }
      ],
      "price": {
        "amount": 1,
        "currency": "string"
      },
      "quantity": 1,
      "startDate": "2026-05-07T12:00:00.000Z",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel.channelId` | string |  |
| `channel.flow` | string |  |
| `channel.name` | string |  |
| `channel.type` | string |  |
| `consumptionId` | string |  |
| `href` | string |  |
| `items[].lookup.country` | string |  |
| `items[].lookup.countryPrefix` | string |  |
| `items[].lookup.isoCountryCode` | string |  |
| `items[].lookup.mcc` | string |  |
| `items[].lookup.mccMnc` | string |  |
| `items[].lookup.mnc` | string |  |
| `items[].lookup.network` | string |  |
| `items[].price.amount` | number |  |
| `items[].price.currency` | string |  |
| `items[].quantity` | number |  |
| `items[].statuses[].quantity` | number |  |
| `items[].statuses[].value` | string |  |
| `price.amount` | number |  |
| `price.currency` | string |  |
| `quantity` | number |  |
| `startDate` | date |  |
| `type` | string |  |

## Native endpoint

Through the native smsmode API, this operation is `GET commons/v1/channels/:channelId/consumptions/:consumptionId` (base URL `https://rest.smsmode.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-consumption.md) for the provider-specific parameters and requirements.

