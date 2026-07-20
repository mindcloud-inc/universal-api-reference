# SparkPost: Check Tracking Domain Certificate Eligibility



```
GET https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/check-tracking-domain-certificate-eligibility
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SparkPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/check-tracking-domain-certificate-eligibility?connectionId=$CONNECTION_ID&domain=track-codex-stage3-20260324.net" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "track-codex-stage3-20260324.net"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/check-tracking-domain-certificate-eligibility?${params}`, {
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
| `domain` | string | yes | Tracking domain to check for managed certificate eligibility. Default: `track-codex-stage3-20260324.net`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "domain": "string",
      "supportsManagedCertificate": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domain` | string |  |
| `supportsManagedCertificate` | boolean |  |

## Native endpoint

Through the native SparkPost API, this operation is `POST /tracking-domains/:domain/certificate/check` (base URL `https://api.sparkpost.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-tracking-domain-certificate-eligibility.md) for the provider-specific parameters and requirements.

