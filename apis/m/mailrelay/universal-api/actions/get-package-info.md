# Mailrelay: Get Package Info

Retrieves package details from your Mailrelay account.

```
GET https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/get-package-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailrelay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/get-package-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/get-package-info?${params}`, {
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
      "billingType": "string",
      "limit": 1,
      "packageType": "string",
      "periodStartDate": "2026-05-07T12:00:00.000Z",
      "subscribersLimit": 1,
      "subscribersUsage": 1,
      "usage": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingType` | string |  |
| `limit` | number |  |
| `packageType` | string |  |
| `periodStartDate` | date |  |
| `subscribersLimit` | number |  |
| `subscribersUsage` | number |  |
| `usage` | number |  |

## Native endpoint

Through the native Mailrelay API, this operation is `GET package` (base URL `https://{{credentials.accountDomain}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-package-info.md) for the provider-specific parameters and requirements.

