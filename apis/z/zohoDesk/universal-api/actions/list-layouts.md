# Zoho Desk: List Layouts

Retrieve a list of all the layouts configured for a module.

```
GET https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/list-layouts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Desk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/list-layouts?connectionId=$CONNECTION_ID&limit=25&offset=0&module=tickets&status=all" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "module": "tickets",
  "status": "all"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/list-layouts?${params}`, {
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
| `module` | list<string> | yes | Name of the module whose layouts must be fetched. One of: `accounts`, `calls`, `contacts`, `contracts`, `events`, `products`, `tasks`, `tickets`, `timeEntry`. Example: `tickets`. |
| `status` | list<string> | yes | Status of the layout. Default: `active`. Example: `all`. |
| `layoutName` | string | no | Name of the layout. Example: `My Test Layout`. |
| `id` | number | no | Example: `903940000000805577`. |
| `departmentId` | number | no | Example: `903940000000805577`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdBy": 1,
      "createdTime": "2026-05-07T12:00:00.000Z",
      "departmentId": 1,
      "hasLogo": true,
      "id": 1,
      "isDefaultLayout": true,
      "isStandardLayout": true,
      "layoutDesc": "string",
      "layoutDisplayName": "Ava Chen",
      "layoutName": "Ava Chen",
      "layoutProfiles": [
        {
          "id": 1,
          "isDefault": true,
          "profileName": "Ava Chen",
          "type": "string"
        }
      ],
      "modifiedBy": 1,
      "modifiedTime": "2026-05-07T12:00:00.000Z",
      "module": "string",
      "photoURL": "https://example.com",
      "skipDeptAccessValidation": true,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdBy` | number |  |
| `createdTime` | date |  |
| `departmentId` | number |  |
| `hasLogo` | boolean |  |
| `id` | number |  |
| `isDefaultLayout` | boolean |  |
| `isStandardLayout` | boolean |  |
| `layoutDesc` | string |  |
| `layoutDisplayName` | string |  |
| `layoutName` | string |  |
| `layoutProfiles[].id` | number |  |
| `layoutProfiles[].isDefault` | boolean |  |
| `layoutProfiles[].profileName` | string |  |
| `layoutProfiles[].type` | string |  |
| `modifiedBy` | number |  |
| `modifiedTime` | date |  |
| `module` | string |  |
| `photoURL` | string |  |
| `skipDeptAccessValidation` | boolean |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho Desk API, this operation is `GET layouts` (base URL `https://desk.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-layouts.md) for the provider-specific parameters and requirements.

