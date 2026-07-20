# Testlify: Create Access Token

Creates a new access token in Testlify.

```
POST https://connect.mindcloud.co/v1/universal/testlify/latest/actions/create-access-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Testlify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/testlify/latest/actions/create-access-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/testlify/latest/actions/create-access-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `note` | string | no | Descriptive note for the access token. |
| `expiration` | date | no | Token expiration timestamp in ISO 8601 format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessToken": "string",
      "created": "string",
      "createdBy": "string",
      "expiration": "string",
      "id": "string",
      "modified": "string",
      "note": "string",
      "orgId": "string",
      "status": "string",
      "userIdentifierId": "string",
      "userWorkspaceProfileId": "string",
      "workspaceUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessToken` | string |  |
| `created` | string |  |
| `createdBy` | string |  |
| `expiration` | string |  |
| `id` | string |  |
| `modified` | string |  |
| `note` | string |  |
| `orgId` | string |  |
| `status` | string |  |
| `userIdentifierId` | string |  |
| `userWorkspaceProfileId` | string |  |
| `workspaceUrl` | string |  |

## Native endpoint

Through the native Testlify API, this operation is `POST /v1/workspace/accesstoken/generate` (base URL `https://api.testlify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-access-token.md) for the provider-specific parameters and requirements.

