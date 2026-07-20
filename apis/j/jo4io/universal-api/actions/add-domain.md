# jo4.io: Add Domain



```
POST https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/add-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a jo4.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/add-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domain": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/add-domain', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domain": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domain` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cnameTarget": "Ava Chen",
      "createdTime": 1,
      "dnsTxtRecordName": "Ava Chen",
      "dnsTxtRecordValue": "string",
      "domain": "string",
      "hostnameStatus": "Ava Chen",
      "id": 1,
      "modifiedTime": 1,
      "ready": true,
      "slug": "string",
      "sslProvisionedAt": 1,
      "sslStatus": "string",
      "sslTxtName": "Ava Chen",
      "sslTxtValue": "string",
      "userId": 1,
      "verified": true,
      "verifiedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cnameTarget` | string |  |
| `createdTime` | number |  |
| `dnsTxtRecordName` | string |  |
| `dnsTxtRecordValue` | string |  |
| `domain` | string |  |
| `hostnameStatus` | string |  |
| `id` | number |  |
| `modifiedTime` | number |  |
| `ready` | boolean |  |
| `slug` | string |  |
| `sslProvisionedAt` | number |  |
| `sslStatus` | string |  |
| `sslTxtName` | string |  |
| `sslTxtValue` | string |  |
| `userId` | number |  |
| `verified` | boolean |  |
| `verifiedAt` | number |  |

## Native endpoint

Through the native jo4.io API, this operation is `POST /protected/domains` (base URL `https://jo4-api.jo4.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-domain.md) for the provider-specific parameters and requirements.

