# Zoho Assist: List Unattended Computers

Lists unattended computers configured in Zoho Assist.

```
GET https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/list-unattended-computers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Assist `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/list-unattended-computers?connectionId=$CONNECTION_ID&limit=25&offset=0&departmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "departmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/list-unattended-computers?${params}`, {
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
| `departmentId` | string | yes |  |
| `source` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addedBy": "string",
      "addedTime": "string",
      "deviceInfo": {},
      "displayName": "Ava Chen",
      "platformDetails": {},
      "resourceId": "string",
      "updatedTime": "string",
      "ursKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addedBy` | string |  |
| `addedTime` | string |  |
| `deviceInfo` | object |  |
| `displayName` | string |  |
| `platformDetails` | object |  |
| `resourceId` | string |  |
| `updatedTime` | string |  |
| `ursKey` | string |  |

## Native endpoint

Through the native Zoho Assist API, this operation is `GET /devices` (base URL `https://assist.zoho.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-unattended-computers.md) for the provider-specific parameters and requirements.

