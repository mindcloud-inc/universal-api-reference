# Zoho Assist: Create Unattended Group

Creates a new unattended computer group in Zoho Assist.

```
POST https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/create-unattended-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Assist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/create-unattended-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "departmentId": "string",
  "groupName": "Ava Chen",
  "description": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/create-unattended-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "departmentId": "string",
    "groupName": "Ava Chen",
    "description": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `departmentId` | string | yes | Department in which the group should be created. |
| `groupName` | string | yes | Name of the unattended group. |
| `description` | string | yes | Description for the unattended group. |
| `computerList[]` | array<string> | no | Optional list of device IDs to add to the group. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdBy": 1,
      "createdTime": 1,
      "departmentId": 1,
      "description": "string",
      "groupId": "string",
      "groupName": "Ava Chen",
      "groupType": 1,
      "ursGroupId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdBy` | number |  |
| `createdTime` | number |  |
| `departmentId` | number |  |
| `description` | string |  |
| `groupId` | string |  |
| `groupName` | string |  |
| `groupType` | number |  |
| `ursGroupId` | number |  |

## Native endpoint

Through the native Zoho Assist API, this operation is `POST /unattended_computer/group` (base URL `https://assist.zoho.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-unattended-group.md) for the provider-specific parameters and requirements.

