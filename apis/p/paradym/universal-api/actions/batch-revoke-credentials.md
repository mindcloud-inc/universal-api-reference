# Paradym: Batch Revoke Credentials

Revokes issued credentials in bulk in Paradym.

```
PUT https://connect.mindcloud.co/v1/universal/paradym/latest/actions/batch-revoke-credentials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paradym `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/paradym/latest/actions/batch-revoke-credentials" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "issuedCredentialIds[0]": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paradym/latest/actions/batch-revoke-credentials', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "issuedCredentialIds[0]": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `issuedCredentialIds[0]` | string | yes |  |
| `issuedCredentialIds[1]` | string | no |  |
| `issuedCredentialIds[2]` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Paradym API returns.

## Native endpoint

Through the native Paradym API, this operation is `POST /projects/:projectId/revocation/batch` (base URL `https://api.paradym.id/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-revoke-credentials.md) for the provider-specific parameters and requirements.

