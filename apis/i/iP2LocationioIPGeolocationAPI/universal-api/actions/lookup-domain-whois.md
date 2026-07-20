# IP2Location.io IP Geolocation: Lookup Domain WHOIS

Retrieves domain WHOIS details from IP2Location.io by domain name.

```
GET https://connect.mindcloud.co/v1/universal/iP2LocationioIPGeolocationAPI/latest/actions/lookup-domain-whois
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IP2Location.io IP Geolocation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iP2LocationioIPGeolocationAPI/latest/actions/lookup-domain-whois?connectionId=$CONNECTION_ID&domain=example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iP2LocationioIPGeolocationAPI/latest/actions/lookup-domain-whois?${params}`, {
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
| `domain` | string | yes | Domain name to look up. Example: `example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "admin": {},
      "billing": {},
      "createDate": "string",
      "domain": "string",
      "domainAge": 1,
      "domainId": "string",
      "expireDate": "string",
      "nameservers": [
        "Ava Chen"
      ],
      "registrant": {},
      "registrar": {},
      "status": "string",
      "tech": {},
      "updateDate": "string",
      "whoisServer": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `admin` | object |  |
| `billing` | object |  |
| `createDate` | string |  |
| `domain` | string |  |
| `domainAge` | number |  |
| `domainId` | string |  |
| `expireDate` | string |  |
| `nameservers` | array<string> |  |
| `registrant` | object |  |
| `registrar` | object |  |
| `status` | string |  |
| `tech` | object |  |
| `updateDate` | string |  |
| `whoisServer` | string |  |

## Native endpoint

Through the native IP2Location.io IP Geolocation API, this operation is `GET https://api.ip2whois.com/v2` (base URL `https://api.ip2location.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-domain-whois.md) for the provider-specific parameters and requirements.

