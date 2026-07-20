# Vortex: List Open Invitations For Invitee



```
GET https://connect.mindcloud.co/v1/universal/vortex/latest/actions/list-open-invitations-for-invitee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vortex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vortex/latest/actions/list-open-invitations-for-invitee?connectionId=$CONNECTION_ID&targetType=string&targetValue=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "targetType": "string",
  "targetValue": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vortex/latest/actions/list-open-invitations-for-invitee?${params}`, {
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
| `targetType` | string | yes | Invitee target type. |
| `targetValue` | string | yes | Invitee target value, such as an email address or phone number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "invitations": [
        {
          "accountId": "string",
          "createdAt": "string",
          "deactivated": true,
          "expired": true,
          "expires": "string",
          "id": "string",
          "invitationType": "string",
          "modifiedAt": "string",
          "scope": "string",
          "scopeType": "string",
          "status": "string",
          "target": [
            {
              "avatarUrl": "https://example.com",
              "name": "Ava Chen",
              "type": "string",
              "value": "string"
            }
          ]
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `invitations[].accountId` | string |  |
| `invitations[].createdAt` | string |  |
| `invitations[].deactivated` | boolean |  |
| `invitations[].expired` | boolean |  |
| `invitations[].expires` | string |  |
| `invitations[].id` | string |  |
| `invitations[].invitationType` | string |  |
| `invitations[].modifiedAt` | string |  |
| `invitations[].scope` | string |  |
| `invitations[].scopeType` | string |  |
| `invitations[].status` | string |  |
| `invitations[].target[].avatarUrl` | string |  |
| `invitations[].target[].name` | string |  |
| `invitations[].target[].type` | string |  |
| `invitations[].target[].value` | string |  |

## Native endpoint

Through the native Vortex API, this operation is `GET /api/v1/invitations` (base URL `https://api.vortexsoftware.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-open-invitations-for-invitee.md) for the provider-specific parameters and requirements.

