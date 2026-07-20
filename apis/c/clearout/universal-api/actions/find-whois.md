# Clearout: Find Whois

Retrieves Whois records for a domain from Clearout.

```
GET https://connect.mindcloud.co/v1/universal/clearout/latest/actions/find-whois
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clearout `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clearout/latest/actions/find-whois?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clearout/latest/actions/find-whois?${params}`, {
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
| `domain` | string | yes | Find Whois record for domain |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `timeout` | number | no | Request wait time (in milliseconds), Maximum allowed wait time should not exceed 110000 milliseconds Default: `90000`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "domain": "string",
      "timeTaken": 1,
      "verifiedOn": "2026-05-07T12:00:00.000Z",
      "whoisRecord": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domain` | string |  |
| `timeTaken` | number |  |
| `verifiedOn` | date |  |
| `whoisRecord` | object |  |

## Native endpoint

Through the native Clearout API, this operation is `POST /domain/resolve/whois` (base URL `https://api.clearout.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-whois.md) for the provider-specific parameters and requirements.

