# Zoho Assist: Get Device Details

Gets details for an unattended device in Zoho Assist.

```
GET https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/get-device-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Assist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/get-device-details?connectionId=$CONNECTION_ID&resourceId=string&departmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resourceId": "string",
  "departmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/get-device-details?${params}`, {
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
| `resourceId` | string | yes | Device resource ID to fetch. |
| `departmentId` | string | yes | Department containing the target device. |
| `source` | string | no | Optional request source tag sent as a Zoho Assist header. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credentials": [
        {}
      ],
      "department": {},
      "deviceInfo": {},
      "displayName": "Ava Chen",
      "domainDetails": {},
      "favourite": true,
      "groups": [
        {}
      ],
      "lastAccessedBy": "string",
      "lastAccessedTime": 1,
      "loggedOnUsers": [
        {}
      ],
      "manufacturerDetails": {},
      "networkDetails": {},
      "platformDetails": {},
      "ursKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credentials` | array<object> | Stored credentials associated with the device. |
| `department` | object | Department information for the device. |
| `deviceInfo` | object | Device identity and status details. |
| `displayName` | string | Display name of the device. |
| `domainDetails` | object | Domain membership details. |
| `favourite` | boolean | Whether the device is marked as a favourite. |
| `groups` | array<object> | Groups that include the device. |
| `lastAccessedBy` | string | User who last accessed the device. |
| `lastAccessedTime` | number | Unix timestamp of the last device access. |
| `loggedOnUsers` | array<object> | Users currently or recently logged on to the device. |
| `manufacturerDetails` | object | Manufacturer and product details. |
| `networkDetails` | object | Network details for the device. |
| `platformDetails` | object | Operating system details. |
| `ursKey` | string | Unique unattended device key. |

## Native endpoint

Through the native Zoho Assist API, this operation is `GET /devices/:resourceId` (base URL `https://assist.zoho.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-device-details.md) for the provider-specific parameters and requirements.

