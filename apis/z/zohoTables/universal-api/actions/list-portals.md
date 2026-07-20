# Zoho Tables: List Portals

Retrieves all portals from Zoho Tables.

```
GET https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/list-portals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Tables `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/list-portals?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/list-portals?${params}`, {
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
      "createdByMailId": "string",
      "createdTime": 1,
      "isHomePortal": true,
      "isShared": true,
      "lastModifiedBy": "string",
      "lastModifiedByMailId": "string",
      "lastModifiedTime": 1,
      "name": "Ava Chen",
      "planType": "string",
      "portalId": "string",
      "usersCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdBy` | string | Portal creator name. |
| `createdByMailId` | string | Portal creator email. |
| `createdTime` | number | Portal creation timestamp. |
| `isHomePortal` | boolean | Whether this is the home portal. |
| `isShared` | boolean | Whether the portal is shared. |
| `lastModifiedBy` | string | Last modifier name. |
| `lastModifiedByMailId` | string | Last modifier email. |
| `lastModifiedTime` | number | Portal last modified timestamp. |
| `name` | string | Portal name. |
| `planType` | string | Portal plan type. |
| `portalId` | string | Zoho portal identifier. |
| `usersCount` | number | Number of users in the portal. |

## Native endpoint

Through the native Zoho Tables API, this operation is `GET /portals` (base URL `https://tables.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-portals.md) for the provider-specific parameters and requirements.

