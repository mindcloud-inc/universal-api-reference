# BunnyCDN: Issue Wildcard Certificate

Issues a wildcard certificate for a BunnyCDN DNS zone.

```
POST https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/issue-wildcard-certificate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BunnyCDN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/issue-wildcard-certificate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "zoneId": "string",
  "domain": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/issue-wildcard-certificate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "zoneId": "string",
    "domain": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `zoneId` | string | yes | The Bunny DNS zone ID. |
| `domain` | string | yes | The wildcard domain that the certificate should be issued for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ErrorKey": "string",
      "Field": "string",
      "Message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ErrorKey` | string |  |
| `Field` | string |  |
| `Message` | string |  |

## Native endpoint

Through the native BunnyCDN API, this operation is `POST /dnszone/:zoneId/certificate/issue` (base URL `https://api.bunny.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/issue-wildcard-certificate.md) for the provider-specific parameters and requirements.

