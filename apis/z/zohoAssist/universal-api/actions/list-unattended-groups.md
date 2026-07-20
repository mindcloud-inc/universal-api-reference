# Zoho Assist: List Unattended Groups

Lists existing unattended computer groups in Zoho Assist.

```
GET https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/list-unattended-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Assist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/list-unattended-groups?connectionId=$CONNECTION_ID&departmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "departmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/list-unattended-groups?${params}`, {
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
| `departmentId` | string | yes | Department in which the group exists. |
| `q` | string | no | Optional name filter for groups. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "computerCount": 1,
      "createdBy": "string",
      "groupId": "string",
      "groupName": "Ava Chen",
      "options": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `computerCount` | number |  |
| `createdBy` | string |  |
| `groupId` | string |  |
| `groupName` | string |  |
| `options` | boolean |  |

## Native endpoint

Through the native Zoho Assist API, this operation is `GET /unattended_computer/group` (base URL `https://assist.zoho.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-unattended-groups.md) for the provider-specific parameters and requirements.

