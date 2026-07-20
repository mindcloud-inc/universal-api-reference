# Superglue: Get End User Details



```
GET https://connect.mindcloud.co/v1/universal/superglue/latest/actions/get-end-user-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Superglue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superglue/latest/actions/get-end-user-details?connectionId=$CONNECTION_ID&endUserId=550e8400-e29b-41d4-a716-446655440000" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "endUserId": "550e8400-e29b-41d4-a716-446655440000"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superglue/latest/actions/get-end-user-details?${params}`, {
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
| `endUserId` | string | yes | Internal Superglue end-user ID. Example: `550e8400-e29b-41d4-a716-446655440000`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowedSystems": [
        "string"
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "credentials": [
        {
          "hasCredentials": true,
          "systemId": "string",
          "systemName": "Ava Chen"
        }
      ],
      "email": "ava@example.com",
      "externalId": "string",
      "id": "string",
      "metadata": {},
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowedSystems` | array<string> | System IDs this user can access. |
| `createdAt` | date | End user creation timestamp. |
| `credentials` | array<object> | Credential connection status entries for systems. |
| `credentials[].hasCredentials` | boolean | Whether credentials exist for the system. |
| `credentials[].systemId` | string | Credential system ID. |
| `credentials[].systemName` | string | Credential system name. |
| `email` | string | End user email address. |
| `externalId` | string | Application-defined external user ID. |
| `id` | string | Internal Superglue end user ID. |
| `metadata` | object | Custom metadata for the end user. |
| `name` | string | End user display name. |
| `updatedAt` | date | End user update timestamp. |

## Native endpoint

Through the native Superglue API, this operation is `GET /end-users/:endUserId` (base URL `https://api.superglue.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-end-user-details.md) for the provider-specific parameters and requirements.

