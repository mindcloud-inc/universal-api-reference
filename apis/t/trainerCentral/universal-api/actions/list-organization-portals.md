# TrainerCentral: List Organization Portals

Retrieves organization portals from TrainerCentral.

```
GET https://connect.mindcloud.co/v1/universal/trainerCentral/latest/actions/list-organization-portals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrainerCentral `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trainerCentral/latest/actions/list-organization-portals?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trainerCentral/latest/actions/list-organization-portals?${params}`, {
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
      "createdBy": "string",
      "createdTime": "string",
      "currentUserRole": "string",
      "email": "ava@example.com",
      "favIconUrl": "https://example.com",
      "id": "string",
      "links": {
        "categories": "https://example.com",
        "customdomains": "https://example.com",
        "emailDomains": "ava@example.com",
        "languages": "https://example.com",
        "paymentPortals": "https://example.com",
        "signupsetting": "https://example.com",
        "site": "https://example.com",
        "translations": "https://example.com"
      },
      "orgLogoUrl": "https://example.com",
      "planName": "Ava Chen",
      "portalName": "Ava Chen",
      "publishStatus": "string",
      "url": "https://example.com",
      "zsoid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdBy` | string |  |
| `createdTime` | string |  |
| `currentUserRole` | string |  |
| `email` | string |  |
| `favIconUrl` | string |  |
| `id` | string |  |
| `links.categories` | string |  |
| `links.customdomains` | string |  |
| `links.emailDomains` | string |  |
| `links.languages` | string |  |
| `links.paymentPortals` | string |  |
| `links.signupsetting` | string |  |
| `links.site` | string |  |
| `links.translations` | string |  |
| `orgLogoUrl` | string |  |
| `planName` | string |  |
| `portalName` | string |  |
| `publishStatus` | string |  |
| `url` | string |  |
| `zsoid` | string |  |

## Native endpoint

Through the native TrainerCentral API, this operation is `GET {{credentials.academyUrl}}/api/v4/org/portals.json` (base URL `{{credentials.academyUrl}}/api/v4/{{credentials.orgId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organization-portals.md) for the provider-specific parameters and requirements.

