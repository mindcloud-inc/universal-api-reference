# Docusnap365: List Systems



```
GET https://connect.mindcloud.co/v1/universal/docusnap365/latest/actions/list-systems
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docusnap365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docusnap365/latest/actions/list-systems?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docusnap365/latest/actions/list-systems?${params}`, {
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
      "buildingId": "string",
      "degId": "string",
      "domainId": "string",
      "firstInventoryTimeUtc": "2026-05-07T12:00:00.000Z",
      "floorId": "string",
      "fqdn": "string",
      "iconId": "string",
      "id": "string",
      "isVirtual": true,
      "jobStartedAtUtc": "2026-05-07T12:00:00.000Z",
      "label": "string",
      "lastInventoryTimeUtc": "2026-05-07T12:00:00.000Z",
      "lastLoggedOnUser": "string",
      "lastUserChangeTimeUtc": "2026-05-07T12:00:00.000Z",
      "module": "string",
      "name": "Ava Chen",
      "organizationId": "string",
      "os": "string",
      "platformId": "string",
      "realm": "string",
      "resourceTypeId": "string",
      "roomId": "string",
      "scope": "string",
      "segment": "string",
      "siteId": "string",
      "status": "string",
      "userDefined": true,
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `buildingId` | string |  |
| `degId` | string |  |
| `domainId` | string |  |
| `firstInventoryTimeUtc` | date |  |
| `floorId` | string |  |
| `fqdn` | string |  |
| `iconId` | string |  |
| `id` | string |  |
| `isVirtual` | boolean |  |
| `jobStartedAtUtc` | date |  |
| `label` | string |  |
| `lastInventoryTimeUtc` | date |  |
| `lastLoggedOnUser` | string |  |
| `lastUserChangeTimeUtc` | date |  |
| `module` | string |  |
| `name` | string |  |
| `organizationId` | string |  |
| `os` | string |  |
| `platformId` | string |  |
| `realm` | string |  |
| `resourceTypeId` | string |  |
| `roomId` | string |  |
| `scope` | string |  |
| `segment` | string |  |
| `siteId` | string |  |
| `status` | string |  |
| `userDefined` | boolean |  |
| `userId` | string |  |

## Native endpoint

Through the native Docusnap365 API, this operation is `GET /api/v2/segment/systems` (base URL `https://api.docusnap365.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-systems.md) for the provider-specific parameters and requirements.

