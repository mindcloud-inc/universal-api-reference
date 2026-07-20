# Referral Rock: Create Member Access URLs

Creates member share and portal URLs in Referral Rock.

```
POST https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/create-member-access-urls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Referral Rock `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/create-member-access-urls" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "memberQuery": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/create-member-access-urls', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "memberQuery": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `expireInMinutes` | number | no | Number of minutes before the member access URLs expire. |
| `memberQuery` | string | yes | Check by member ID, referral code, email address, or external ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fullEmbedUrl": "https://example.com",
      "portalUrl": "https://example.com",
      "referralCode": "string",
      "shareEmbedUrl": "https://example.com",
      "shareUrl": "https://example.com",
      "smsShareUrl": "https://example.com",
      "webShareUrl": "https://example.com",
      "whatsAppShareUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fullEmbedUrl` | string |  |
| `portalUrl` | string |  |
| `referralCode` | string |  |
| `shareEmbedUrl` | string |  |
| `shareUrl` | string |  |
| `smsShareUrl` | string |  |
| `webShareUrl` | string |  |
| `whatsAppShareUrl` | string |  |

## Native endpoint

Through the native Referral Rock API, this operation is `POST /api/memberaccessurls` (base URL `https://api.referralrock.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-member-access-urls.md) for the provider-specific parameters and requirements.

