# Sigma: Get Connection



```
GET https://connect.mindcloud.co/v1/universal/sigma/latest/actions/get-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sigma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sigma/latest/actions/get-connection?connectionId=$CONNECTION_ID&connectionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "connectionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sigma/latest/actions/get-connection?${params}`, {
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
| `connectionId` | string | yes | Sigma connectionId. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "connectionId": "string",
      "createdAt": "string",
      "createdBy": "string",
      "isAuditLog": true,
      "isSample": true,
      "lastActiveAt": "string",
      "name": "Ava Chen",
      "organizationId": "string",
      "type": "string",
      "updatedAt": "string",
      "updatedBy": "string",
      "useOauth": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `connectionId` | string | Sigma connection identifier |
| `createdAt` | string | Created timestamp |
| `createdBy` | string | Creator user id |
| `isAuditLog` | boolean | Whether audit logging is enabled |
| `isSample` | boolean | Whether this is the sample connection |
| `lastActiveAt` | string | Last activity timestamp |
| `name` | string | Connection name |
| `organizationId` | string | Sigma organization identifier |
| `type` | string | Connection type |
| `updatedAt` | string | Updated timestamp |
| `updatedBy` | string | Last updater user id |
| `useOauth` | boolean | Whether OAuth is used |

## Native endpoint

Through the native Sigma API, this operation is `GET /v2/connections/{connectionId}` (base URL `https://aws-api.sigmacomputing.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-connection.md) for the provider-specific parameters and requirements.

