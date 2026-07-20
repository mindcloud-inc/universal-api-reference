# ipdata.co: Get IP Details



```
GET https://connect.mindcloud.co/v1/universal/ipdataco/latest/actions/get-ip-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ipdata.co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ipdataco/latest/actions/get-ip-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ipdataco/latest/actions/get-ip-details?${params}`, {
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
| `ip` | string | no | The IP address to look up. Default: `8.8.8.8`. |
| `fields` | string | no | Comma-separated response fields to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "asn": {
        "asn": "string",
        "domain": "string",
        "name": "Ava Chen",
        "route": "string",
        "type": "string"
      },
      "callingCode": "string",
      "city": {},
      "continentCode": "string",
      "continentName": "Ava Chen",
      "count": "string",
      "countryCode": "string",
      "countryName": "Ava Chen",
      "currency": {
        "code": "string",
        "name": "Ava Chen",
        "native": "string",
        "plural": "string",
        "symbol": "string"
      },
      "emojiFlag": "string",
      "emojiUnicode": "string",
      "flag": "string",
      "ip": "string",
      "isEu": true,
      "languages": [
        {
          "code": "string",
          "name": "Ava Chen",
          "native": "string"
        }
      ],
      "latitude": 1,
      "longitude": 1,
      "postal": {},
      "region": {},
      "regionCode": {},
      "regionType": {},
      "threat": {
        "blocklists": [
          {
            "name": "Ava Chen",
            "site": "string",
            "type": "string"
          }
        ],
        "isAnonymous": true,
        "isBogon": true,
        "isDatacenter": true,
        "isIcloudRelay": true,
        "isKnownAbuser": true,
        "isKnownAttacker": true,
        "isProxy": true,
        "isThreat": true,
        "isTor": true
      },
      "timeZone": {
        "abbr": {},
        "currentTime": {},
        "isDst": {},
        "name": {},
        "offset": {}
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `asn.asn` | string |  |
| `asn.domain` | string |  |
| `asn.name` | string |  |
| `asn.route` | string |  |
| `asn.type` | string |  |
| `callingCode` | string |  |
| `city` | object |  |
| `continentCode` | string |  |
| `continentName` | string |  |
| `count` | string |  |
| `countryCode` | string |  |
| `countryName` | string |  |
| `currency.code` | string |  |
| `currency.name` | string |  |
| `currency.native` | string |  |
| `currency.plural` | string |  |
| `currency.symbol` | string |  |
| `emojiFlag` | string |  |
| `emojiUnicode` | string |  |
| `flag` | string |  |
| `ip` | string |  |
| `isEu` | boolean |  |
| `languages[].code` | string |  |
| `languages[].name` | string |  |
| `languages[].native` | string |  |
| `latitude` | number |  |
| `longitude` | number |  |
| `postal` | object |  |
| `region` | object |  |
| `regionCode` | object |  |
| `regionType` | object |  |
| `threat.blocklists[].name` | string |  |
| `threat.blocklists[].site` | string |  |
| `threat.blocklists[].type` | string |  |
| `threat.isAnonymous` | boolean |  |
| `threat.isBogon` | boolean |  |
| `threat.isDatacenter` | boolean |  |
| `threat.isIcloudRelay` | boolean |  |
| `threat.isKnownAbuser` | boolean |  |
| `threat.isKnownAttacker` | boolean |  |
| `threat.isProxy` | boolean |  |
| `threat.isThreat` | boolean |  |
| `threat.isTor` | boolean |  |
| `timeZone.abbr` | object |  |
| `timeZone.currentTime` | object |  |
| `timeZone.isDst` | object |  |
| `timeZone.name` | object |  |
| `timeZone.offset` | object |  |

## Native endpoint

Through the native ipdata.co API, this operation is `GET /:ip` (base URL `https://api.ipdata.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ip-details.md) for the provider-specific parameters and requirements.

