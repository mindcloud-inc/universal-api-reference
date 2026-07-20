# ipdata.co Universal API Examples

These examples use the MindCloud API key and ipdata.co connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get IP Details



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

Example response:

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

See the full [Get IP Details action reference](actions/get-ip-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ipdataco/latest/actions/get-ip-details).
