# Sigma: List Account Type Permissions



```
GET https://connect.mindcloud.co/v1/universal/sigma/latest/actions/list-account-type-permissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sigma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sigma/latest/actions/list-account-type-permissions?connectionId=$CONNECTION_ID&accountTypeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountTypeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sigma/latest/actions/list-account-type-permissions?${params}`, {
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
| `accountTypeId` | string | yes | Sigma accountTypeId. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "permission": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Permission description |
| `permission` | string | Permission name for the account type |

## Native endpoint

Through the native Sigma API, this operation is `GET /v2/accountTypes/{accountTypeId}/permissions` (base URL `https://aws-api.sigmacomputing.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-account-type-permissions.md) for the provider-specific parameters and requirements.

