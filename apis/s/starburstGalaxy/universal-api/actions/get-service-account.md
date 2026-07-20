# Starburst Galaxy: Get service account



```
GET https://connect.mindcloud.co/v1/universal/starburstGalaxy/latest/actions/get-service-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starburst Galaxy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starburstGalaxy/latest/actions/get-service-account?connectionId=$CONNECTION_ID&serviceAccountId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "serviceAccountId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/starburstGalaxy/latest/actions/get-service-account?${params}`, {
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
| `serviceAccountId` | string | yes | Starburst Galaxy service account ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "additionalRoleIds": [
        "string"
      ],
      "roleId": "string",
      "serviceAccountId": "string",
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additionalRoleIds` | array<string> |  |
| `roleId` | string |  |
| `serviceAccountId` | string |  |
| `userName` | string |  |

## Native endpoint

Through the native Starburst Galaxy API, this operation is `GET /public/api/v1/serviceAccount/{serviceAccountId}` (base URL `https://mindcloud.galaxy.starburst.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-service-account.md) for the provider-specific parameters and requirements.

