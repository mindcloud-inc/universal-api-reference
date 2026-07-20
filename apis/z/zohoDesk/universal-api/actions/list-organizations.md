# Zoho Desk: List Organizations



```
GET https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Desk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/list-organizations?${params}`, {
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
      "companyName": "Ava Chen",
      "currencyCode": "string",
      "currencySymbol": "string",
      "edition": "string",
      "employeeCount": 1,
      "id": 1,
      "isSandboxPortal": true,
      "portalName": "Ava Chen",
      "portalURL": "https://example.com",
      "primaryContact": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyName` | string |  |
| `currencyCode` | string |  |
| `currencySymbol` | string |  |
| `edition` | string |  |
| `employeeCount` | number |  |
| `id` | number |  |
| `isSandboxPortal` | boolean |  |
| `portalName` | string |  |
| `portalURL` | string |  |
| `primaryContact` | string |  |

## Native endpoint

Through the native Zoho Desk API, this operation is `GET /organizations` (base URL `https://desk.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

