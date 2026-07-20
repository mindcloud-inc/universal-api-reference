# Docusnap365: List Networks By Type



```
GET https://connect.mindcloud.co/v1/universal/docusnap365/latest/actions/list-networks-by-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docusnap365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docusnap365/latest/actions/list-networks-by-type?connectionId=$CONNECTION_ID&typeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "typeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docusnap365/latest/actions/list-networks-by-type?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `typeId` | string | yes | The Docusnap365 network type ID to filter by. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "domainId": "string",
      "firstInventoryTimeUtc": "2026-05-07T12:00:00.000Z",
      "iconId": "string",
      "id": "string",
      "jobStartedAtUtc": "2026-05-07T12:00:00.000Z",
      "label": "string",
      "lastInventoryTimeUtc": "2026-05-07T12:00:00.000Z",
      "lastUserChangeTimeUtc": "2026-05-07T12:00:00.000Z",
      "module": "string",
      "name": "Ava Chen",
      "organizationId": "string",
      "platformId": "string",
      "realm": "string",
      "resourceTypeId": "string",
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
| `description` | string |  |
| `domainId` | string |  |
| `firstInventoryTimeUtc` | date |  |
| `iconId` | string |  |
| `id` | string |  |
| `jobStartedAtUtc` | date |  |
| `label` | string |  |
| `lastInventoryTimeUtc` | date |  |
| `lastUserChangeTimeUtc` | date |  |
| `module` | string |  |
| `name` | string |  |
| `organizationId` | string |  |
| `platformId` | string |  |
| `realm` | string |  |
| `resourceTypeId` | string |  |
| `scope` | string |  |
| `segment` | string |  |
| `siteId` | string |  |
| `status` | string |  |
| `userDefined` | boolean |  |
| `userId` | string |  |

## Native endpoint

Through the native Docusnap365 API, this operation is `GET /api/v2/segment/networks/type/:typeId` (base URL `https://api.docusnap365.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-networks-by-type.md) for the provider-specific parameters and requirements.

