# Zoho Invoice: List Organizations

Retrieves organizations from Zoho Invoice.

```
GET https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Invoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/list-organizations?${params}`, {
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
      "contactName": "Ava Chen",
      "country": "string",
      "countryCode": "string",
      "currencyCode": "string",
      "currencySymbol": "string",
      "email": "ava@example.com",
      "isOrgActive": true,
      "name": "Ava Chen",
      "organizationId": "string",
      "orgType": "string",
      "timeZone": "string",
      "timeZoneFormatted": "string",
      "version": "string",
      "versionFormatted": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactName` | string |  |
| `country` | string |  |
| `countryCode` | string |  |
| `currencyCode` | string |  |
| `currencySymbol` | string |  |
| `email` | string |  |
| `isOrgActive` | boolean |  |
| `name` | string |  |
| `organizationId` | string |  |
| `orgType` | string |  |
| `timeZone` | string |  |
| `timeZoneFormatted` | string |  |
| `version` | string |  |
| `versionFormatted` | string |  |

## Native endpoint

Through the native Zoho Invoice API, this operation is `GET /organizations` (base URL `https://www.zohoapis.com/invoice/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

