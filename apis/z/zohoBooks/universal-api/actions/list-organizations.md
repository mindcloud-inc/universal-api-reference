# Zoho Books: List Organizations



```
GET https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Books `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/list-organizations?${params}`, {
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
      "appList": [
        "string"
      ],
      "contactName": "Ava Chen",
      "country": "string",
      "countryCode": "string",
      "currencyCode": "string",
      "currencyId": "string",
      "currencySymbol": "string",
      "email": "ava@example.com",
      "isDefaultOrg": true,
      "isOrgActive": true,
      "languageCode": "string",
      "mode": "string",
      "name": "Ava Chen",
      "organizationId": "string",
      "orgType": "string",
      "planName": "Ava Chen",
      "pricePrecision": 1,
      "state": "string",
      "stateCode": "string",
      "timeZone": "string",
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
| `appList` | array<string> |  |
| `contactName` | string |  |
| `country` | string |  |
| `countryCode` | string |  |
| `currencyCode` | string |  |
| `currencyId` | string |  |
| `currencySymbol` | string |  |
| `email` | string |  |
| `isDefaultOrg` | boolean |  |
| `isOrgActive` | boolean |  |
| `languageCode` | string |  |
| `mode` | string |  |
| `name` | string |  |
| `organizationId` | string |  |
| `orgType` | string |  |
| `planName` | string |  |
| `pricePrecision` | number |  |
| `state` | string |  |
| `stateCode` | string |  |
| `timeZone` | string |  |
| `version` | string |  |
| `versionFormatted` | string |  |

## Native endpoint

Through the native Zoho Books API, this operation is `GET /organizations` (base URL `https://www.zohoapis.com/books/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

