# Zoho People: Get Organization Info

Retrieves organization details from Zoho People.

```
GET https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/get-organization-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho People `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/get-organization-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/get-organization-info?${params}`, {
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
      "address": {
        "addressLine1": "string",
        "addressLine2": "string",
        "city": "string",
        "country": "string",
        "postalCode": "string",
        "state": "string"
      },
      "contactMailId": "string",
      "contactNumber": "string",
      "contactPerson": "string",
      "dateFormat": "string",
      "timeFormat": "string",
      "timeZone": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address.addressLine1` | string |  |
| `address.addressLine2` | string |  |
| `address.city` | string |  |
| `address.country` | string |  |
| `address.postalCode` | string |  |
| `address.state` | string |  |
| `contactMailId` | string |  |
| `contactNumber` | string |  |
| `contactPerson` | string |  |
| `dateFormat` | string |  |
| `timeFormat` | string |  |
| `timeZone` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Zoho People API, this operation is `GET /api/v3/organization` (base URL `https://people.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization-info.md) for the provider-specific parameters and requirements.

