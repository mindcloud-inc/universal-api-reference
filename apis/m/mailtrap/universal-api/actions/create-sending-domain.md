# Mailtrap: Create Sending Domain

Creates a new sending domain in Mailtrap.

```
POST https://connect.mindcloud.co/v1/universal/mailtrap/latest/actions/create-sending-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailtrap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailtrap/latest/actions/create-sending-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailtrap/latest/actions/create-sending-domain', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "complianceStatus": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dnsVerified": true,
      "domainName": "Ava Chen",
      "id": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `complianceStatus` | string |  |
| `createdAt` | date |  |
| `dnsVerified` | boolean |  |
| `domainName` | string |  |
| `id` | number |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Mailtrap API, this operation is `POST /sending_domains` (base URL `https://mailtrap.io/api/accounts/:account_id`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sending-domain.md) for the provider-specific parameters and requirements.

