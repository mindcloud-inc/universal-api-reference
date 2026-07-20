# jo4.io: List Domains



```
GET https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/get-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a jo4.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/get-domains?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/get-domains?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native jo4.io API, this operation is `GET /protected/domains` (base URL `https://jo4-api.jo4.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-domains.md) for the provider-specific parameters and requirements.

