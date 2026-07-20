# WhoisJson: Get Whois Data

Retrieves WHOIS data for a domain from WhoisJson.

```
GET https://connect.mindcloud.co/v1/universal/whoisJson/latest/actions/get-whois-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhoisJson `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whoisJson/latest/actions/get-whois-data?connectionId=$CONNECTION_ID&domain=example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whoisJson/latest/actions/get-whois-data?${params}`, {
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
| `format` | string | no | Optional response format. WhoisJSON documents json and xml. Default: `json`. Example: `json`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "changed": "2026-05-07T12:00:00.000Z",
      "created": "2026-05-07T12:00:00.000Z",
      "expires": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "nameserver": [
        "Ava Chen"
      ],
      "registered": true,
      "registrar": {
        "name": "Ava Chen",
        "url": "https://example.com"
      },
      "status": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `changed` | date |  |
| `created` | date |  |
| `expires` | date |  |
| `name` | string |  |
| `nameserver[]` | string |  |
| `registered` | boolean |  |
| `registrar.name` | string |  |
| `registrar.url` | string |  |
| `status[]` | string |  |

## Native endpoint

Through the native WhoisJson API, this operation is `GET /whois` (base URL `https://whoisjson.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-whois-data.md) for the provider-specific parameters and requirements.

