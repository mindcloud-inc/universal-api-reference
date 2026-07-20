# OOPSpam: Check Content for Spam

Checks submitted content for spam in OOPSpam.

```
POST https://connect.mindcloud.co/v1/universal/oOPSpam/latest/actions/check-content-for-spam
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OOPSpam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oOPSpam/latest/actions/check-content-for-spam" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oOPSpam/latest/actions/check-content-for-spam', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | string | no | Message content to analyze for spam. |
| `senderIP` | string | no | IP address of the original sender. |
| `email` | string | no | Email address of the original sender. |
| `checkForLength` | boolean | no | Treat very short content as spam. Default: `true`. |
| `blockTempEmail` | boolean | no | Block disposable email addresses. Default: `false`. |
| `logIt` | boolean | no | Send this request to OOPSpam dashboard logs. Default: `false`. |
| `source` | string | no | Unique source identifier required when logIt is true. |
| `context` | string | no | Business or website context used for contextual detection. |
| `blockVPN` | boolean | no | Block VPN, proxy, and Tor IPs. Default: `false`. |
| `blockDC` | boolean | no | Block cloud provider and data center IPs. Default: `false`. |
| `urlFriendly` | boolean | no | Reduce the impact of links on the spam score. Default: `false`. |
| `allowedLanguages[]` | array<string> | no | Two-letter language codes that are allowed. |
| `allowedCountries[]` | array<string> | no | Two-letter country codes that are allowed. |
| `blockedCountries[]` | array<string> | no | Two-letter country codes that are blocked. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "details": {
        "isEmailBlocked": true,
        "numberOfSpamWords": 1
      },
      "score": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details.isEmailBlocked` | boolean |  |
| `details.numberOfSpamWords` | number |  |
| `score` | number |  |

## Native endpoint

Through the native OOPSpam API, this operation is `POST /spamdetection` (base URL `https://api.oopspam.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-content-for-spam.md) for the provider-specific parameters and requirements.

