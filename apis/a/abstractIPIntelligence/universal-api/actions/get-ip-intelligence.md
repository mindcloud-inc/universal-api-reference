# Abstract IP Intelligence: Get IP Intelligence

Retrieves IP intelligence from Abstract IP Intelligence.

```
GET https://connect.mindcloud.co/v1/universal/abstractIPIntelligence/latest/actions/get-ip-intelligence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Abstract IP Intelligence `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/abstractIPIntelligence/latest/actions/get-ip-intelligence?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/abstractIPIntelligence/latest/actions/get-ip-intelligence?${params}`, {
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
| `ipAddress` | string | no | IPv4 or IPv6 address to analyze. Leave blank to let Abstract infer the caller IP. Example: `166.171.248.255`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields` | string | no | Comma-separated top-level response sections to return Accepts multiple values in one string, delimited by `,`. Example: `location,security`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "asn": {},
      "company": {},
      "currency": {},
      "domains": {},
      "flag": {},
      "ip_address": "string",
      "location": {},
      "security": {},
      "timezone": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `asn` | object | Autonomous system details for the IP address. |
| `company` | object | Company or ISP details associated with the IP address. |
| `currency` | object | Currency details for the detected country. |
| `domains` | object | Domains associated with the IP address. |
| `flag` | object | Country flag assets for the detected country. |
| `ip_address` | string | The IP address that was analyzed. |
| `location` | object | Geolocation details for the IP address. |
| `security` | object | Security signals for VPN, proxy, TOR, hosting, relay, mobile, and abuse. |
| `timezone` | object | Timezone details for the analyzed IP address. |

## Native endpoint

Through the native Abstract IP Intelligence API, this operation is `GET /` (base URL `https://ip-intelligence.abstractapi.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ip-intelligence.md) for the provider-specific parameters and requirements.

