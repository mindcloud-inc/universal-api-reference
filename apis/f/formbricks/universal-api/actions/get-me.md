# Formbricks: Get Me

Retrieves the current user from Formbricks.

```
GET https://connect.mindcloud.co/v1/universal/formbricks/latest/actions/get-me
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formbricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formbricks/latest/actions/get-me?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formbricks/latest/actions/get-me?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "environments": [
        {
          "environmentId": "string",
          "environmentType": "string",
          "permission": "string",
          "projectId": "string",
          "projectName": "Ava Chen"
        }
      ],
      "organizationAccess": {
        "accessControl": {
          "read": true,
          "write": true
        }
      },
      "organizationId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `environments` | array<object> | Environments accessible to the API key. |
| `environments[].environmentId` | string | Environment ID. |
| `environments[].environmentType` | string | Environment type such as production. |
| `environments[].permission` | string | Permission granted for the environment. |
| `environments[].projectId` | string | Project ID for the environment. |
| `environments[].projectName` | string | Project name for the environment. |
| `organizationAccess` | object | Organization-level access information for the API key. |
| `organizationAccess.accessControl` | object | Read and write permissions for the organization. |
| `organizationAccess.accessControl.read` | boolean | Whether the API key can read organization resources. |
| `organizationAccess.accessControl.write` | boolean | Whether the API key can write organization resources. |
| `organizationId` | string | Organization ID associated with the API key. |

## Native endpoint

Through the native Formbricks API, this operation is `GET /me` (base URL `https://app.formbricks.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-me.md) for the provider-specific parameters and requirements.

