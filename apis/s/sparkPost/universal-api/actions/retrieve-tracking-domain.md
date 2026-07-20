# SparkPost: Retrieve Tracking Domain



```
GET https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/retrieve-tracking-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SparkPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/retrieve-tracking-domain?connectionId=$CONNECTION_ID&domain=track-codex-stage3-20260324.net" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "track-codex-stage3-20260324.net"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/retrieve-tracking-domain?${params}`, {
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
| `domain` | string | yes | Tracking domain to retrieve. Default: `track-codex-stage3-20260324.net`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "default": true,
      "domain": "string",
      "port": 1,
      "secure": true,
      "status": {},
      "usesManagedCertificate": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `default` | boolean |  |
| `domain` | string |  |
| `port` | number |  |
| `secure` | boolean |  |
| `status` | object |  |
| `usesManagedCertificate` | boolean |  |

## Native endpoint

Through the native SparkPost API, this operation is `GET /tracking-domains/:domain` (base URL `https://api.sparkpost.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-tracking-domain.md) for the provider-specific parameters and requirements.

