# Seam: List Phones

Retrieves a list of phones from Seam.

```
GET https://connect.mindcloud.co/v1/universal/seam/latest/actions/list-phones
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seam/latest/actions/list-phones?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seam/latest/actions/list-phones?${params}`, {
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
| `acsCredentialId` | string | no | ID of the credential by which you want to filter phones. |
| `ownerUserIdentityId` | string | no | ID of the owner user identity by which you want to filter phones. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customMetadata": {},
      "deviceId": "string",
      "deviceType": "string",
      "displayName": "Ava Chen",
      "errors": [
        {}
      ],
      "nickname": "Ava Chen",
      "properties": {},
      "warnings": [
        {}
      ],
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Creation timestamp. |
| `customMetadata` | object | Optional custom metadata for the phone. |
| `deviceId` | string | Unique Seam device ID for the phone. |
| `deviceType` | string | Phone device type, such as `ios_phone` or `android_phone`. |
| `displayName` | string | Display name of the phone. |
| `errors` | array<object> | Errors associated with the phone. |
| `nickname` | string | Optional phone nickname. |
| `properties` | object | Phone-specific properties such as credential-service metadata. |
| `warnings` | array<object> | Warnings associated with the phone. |
| `workspaceId` | string | Workspace that contains the phone. |

## Native endpoint

Through the native Seam API, this operation is `POST /phones/list` (base URL `https://connect.getseam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-phones.md) for the provider-specific parameters and requirements.

