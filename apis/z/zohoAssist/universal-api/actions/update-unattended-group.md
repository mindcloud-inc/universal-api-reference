# Zoho Assist: Update Unattended Group

Updates an existing unattended computer group in Zoho Assist.

```
PUT https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/update-unattended-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Assist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/update-unattended-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "departmentId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/update-unattended-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "departmentId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | ID of the group to update. |
| `departmentId` | string | yes | Department containing the group. |
| `name` | string | yes | Updated group name. |
| `description` | string | no | Updated group description. |
| `addedList[]` | array<string> | no | Optional device IDs to add to the group. |
| `removedList[]` | array<string> | no | Optional device IDs to remove from the group. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "departmentId": 1,
      "description": "string",
      "groupName": "Ava Chen",
      "success": true,
      "ursGroupId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `departmentId` | number |  |
| `description` | string |  |
| `groupName` | string |  |
| `success` | boolean |  |
| `ursGroupId` | string |  |

## Native endpoint

Through the native Zoho Assist API, this operation is `PUT /unattended_computer/group` (base URL `https://assist.zoho.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-unattended-group.md) for the provider-specific parameters and requirements.

