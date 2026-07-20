# Absinthe: Resolve Identity to User ID

Finds a user ID in Absinthe by identity.

```
GET https://connect.mindcloud.co/v1/universal/absinthe/latest/actions/resolve-identity-to-user-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Absinthe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/absinthe/latest/actions/resolve-identity-to-user-id?connectionId=$CONNECTION_ID&identityType=string&identityValue=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identityType": "string",
  "identityValue": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/absinthe/latest/actions/resolve-identity-to-user-id?${params}`, {
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
| `identityType` | string | yes |  |
| `identityValue` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Absinthe API returns.

## Native endpoint

Through the native Absinthe API, this operation is `GET /users/resolve` (base URL `https://api.absinthe.network`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resolve-identity-to-user-id.md) for the provider-specific parameters and requirements.

