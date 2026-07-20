# Cloudmersive: Get Domain WHOIS

Retrieves WHOIS data for a domain in Cloudmersive.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/get-domain-whois
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/get-domain-whois?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/get-domain-whois?${params}`, {
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
| `domain` | string | no | Domain name for the WHOIS lookup. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdDt": "2026-05-07T12:00:00.000Z",
      "rawTextRecord": "string",
      "registrantCity": "string",
      "registrantCountry": "string",
      "registrantEmail": "ava@example.com",
      "registrantName": "Ava Chen",
      "registrantOrganization": "string",
      "registrantPostalCode": "string",
      "registrantStateOrProvince": "string",
      "validDomain": true,
      "whoisServer": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdDt` | date |  |
| `rawTextRecord` | string |  |
| `registrantCity` | string |  |
| `registrantCountry` | string |  |
| `registrantEmail` | string |  |
| `registrantName` | string |  |
| `registrantOrganization` | string |  |
| `registrantPostalCode` | string |  |
| `registrantStateOrProvince` | string |  |
| `validDomain` | boolean |  |
| `whoisServer` | string |  |

## Native endpoint

Through the native Cloudmersive API, this operation is `POST /validate/domain/whois` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-domain-whois.md) for the provider-specific parameters and requirements.

