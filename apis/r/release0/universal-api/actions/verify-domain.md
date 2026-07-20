# Release0: Verify Domain

Checks whether a custom domain is verified in Release0.

```
GET https://connect.mindcloud.co/v1/universal/release0/latest/actions/verify-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Release0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/release0/latest/actions/verify-domain?connectionId=$CONNECTION_ID&name=Ava%20Chen&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen",
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/release0/latest/actions/verify-domain?${params}`, {
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
| `name` | string | yes | The domain name to verify. |
| `workspaceId` | string | yes | The workspace that owns the domain to verify. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "configJson": {
        "misconfigured": true,
        "serviceType": "string"
      },
      "domainJson": {
        "apexName": "Ava Chen",
        "createdAt": 1,
        "name": "Ava Chen",
        "projectId": "string",
        "updatedAt": 1,
        "verified": true
      },
      "verificationJson": {
        "error": {
          "code": "string",
          "message": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `configJson.misconfigured` | boolean |  |
| `configJson.serviceType` | string |  |
| `domainJson.apexName` | string |  |
| `domainJson.createdAt` | number |  |
| `domainJson.name` | string |  |
| `domainJson.projectId` | string |  |
| `domainJson.updatedAt` | number |  |
| `domainJson.verified` | boolean |  |
| `verificationJson.error.code` | string |  |
| `verificationJson.error.message` | string |  |

## Native endpoint

Through the native Release0 API, this operation is `GET /v1/domains/:name/verify` (base URL `https://release0.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-domain.md) for the provider-specific parameters and requirements.

