# ONLYOFFICE DocSpace: Get Portal Information

Retrieves portal information from ONLYOFFICE DocSpace.

```
GET https://connect.mindcloud.co/v1/universal/oNLYOFFICEDocSpace/latest/actions/get-portal-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ONLYOFFICE DocSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oNLYOFFICEDocSpace/latest/actions/get-portal-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oNLYOFFICEDocSpace/latest/actions/get-portal-information?${params}`, {
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
      "calls": true,
      "creationDateTime": "2026-05-07T12:00:00.000Z",
      "industry": 1,
      "language": "string",
      "lastModified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "ownerId": "string",
      "region": "string",
      "spam": true,
      "status": 1,
      "statusChangeDate": "2026-05-07T12:00:00.000Z",
      "tenantAlias": "string",
      "tenantId": 1,
      "timeZone": "string",
      "trustedDomainsType": 1,
      "version": 1,
      "versionChanged": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calls` | boolean |  |
| `creationDateTime` | date |  |
| `industry` | number |  |
| `language` | string |  |
| `lastModified` | date |  |
| `name` | string |  |
| `ownerId` | string |  |
| `region` | string |  |
| `spam` | boolean |  |
| `status` | number |  |
| `statusChangeDate` | date |  |
| `tenantAlias` | string |  |
| `tenantId` | number |  |
| `timeZone` | string |  |
| `trustedDomainsType` | number |  |
| `version` | number |  |
| `versionChanged` | date |  |

## Native endpoint

Through the native ONLYOFFICE DocSpace API, this operation is `GET /api/2.0/portal` (base URL `https://docspace-t0dtrp.onlyoffice.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-portal-information.md) for the provider-specific parameters and requirements.

