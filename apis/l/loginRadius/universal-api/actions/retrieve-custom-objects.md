# LoginRadius: Retrieve Custom Objects

Retrieves custom object records from LoginRadius.

```
GET https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/retrieve-custom-objects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoginRadius `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/retrieve-custom-objects?connectionId=$CONNECTION_ID&accessToken=string&objectName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accessToken": "string",
  "objectName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/retrieve-custom-objects?${params}`, {
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
| `accessToken` | string | yes | Access token of the user. |
| `objectName` | string | yes | Configured custom object name. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customObjectId` | string | no | Specific custom object record ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native LoginRadius API returns.

## Native endpoint

Through the native LoginRadius API, this operation is `GET /identity/v2/auth/customobject` (base URL `https://api.loginradius.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-custom-objects.md) for the provider-specific parameters and requirements.

