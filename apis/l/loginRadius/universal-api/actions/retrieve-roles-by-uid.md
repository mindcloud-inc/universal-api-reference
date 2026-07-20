# LoginRadius: Retrieve Roles by UID

Retrieves assigned roles from LoginRadius by UID.

```
GET https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/retrieve-roles-by-uid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoginRadius `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/retrieve-roles-by-uid?connectionId=$CONNECTION_ID&uid=743a88db13d1411b9a0c68d7218f1703" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uid": "743a88db13d1411b9a0c68d7218f1703"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/retrieve-roles-by-uid?${params}`, {
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
| `uid` | string | yes | UID of the user. Example: `743a88db13d1411b9a0c68d7218f1703`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "roles": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `roles[]` | string |  |

## Native endpoint

Through the native LoginRadius API, this operation is `GET /identity/v2/manage/account/:uid/role` (base URL `https://api.loginradius.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-roles-by-uid.md) for the provider-specific parameters and requirements.

