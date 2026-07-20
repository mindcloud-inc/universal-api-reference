# Zoho Tables: List Base

Retrieves all bases from Zoho Tables.

```
GET https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/list-base
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Tables `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/list-base?connectionId=$CONNECTION_ID&portalId=1&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "portalId": "1",
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/list-base?${params}`, {
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
| `portalId` | number | yes | Portal ID |
| `workspaceId` | string | yes | Workspace ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "baseId": "string",
      "color": "string",
      "createdBy": "string",
      "createdByMailId": "string",
      "createdTime": 1,
      "icon": 1,
      "lastModifiedBy": "string",
      "lastModifiedByMailId": "string",
      "lastModifiedTime": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseId` | string | Zoho base identifier. |
| `color` | string | Base color token. |
| `createdBy` | string | Base creator name. |
| `createdByMailId` | string | Base creator email. |
| `createdTime` | number | Base creation timestamp. |
| `icon` | number | Base icon code. |
| `lastModifiedBy` | string | Last modifier name. |
| `lastModifiedByMailId` | string | Last modifier email. |
| `lastModifiedTime` | number | Base last modified timestamp. |
| `name` | string | Base name. |

## Native endpoint

Through the native Zoho Tables API, this operation is `GET /bases` (base URL `https://tables.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-base.md) for the provider-specific parameters and requirements.

