# FuseDesk: Create Case

Creates a new case in FuseDesk.

```
POST https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/create-case
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FuseDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/create-case" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "departmentId": 1,
  "details": "string",
  "openedBy": "string",
  "summary": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/create-case', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "departmentId": 1,
    "details": "string",
    "openedBy": "string",
    "summary": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `caseTags` | string | no |  |
| `companyId` | number | no |  |
| `contactId` | number | no |  |
| `contactUuid` | string | no |  |
| `dateAssigned` | string | no |  |
| `dateOpened` | string | no |  |
| `departmentId` | number | yes |  |
| `details` | string | yes |  |
| `openedBy` | string | yes |  |
| `repId` | number | no |  |
| `status` | string | no |  |
| `summary` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native FuseDesk API returns.

## Native endpoint

Through the native FuseDesk API, this operation is `POST /api/v1/cases` (base URL `https://{{credentials.appName}}.fusedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-case.md) for the provider-specific parameters and requirements.

