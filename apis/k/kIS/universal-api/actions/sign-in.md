# KIS: Sign In

Signs in to the KIS API.

```
GET https://connect.mindcloud.co/v1/universal/kIS/latest/actions/sign-in
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KIS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kIS/latest/actions/sign-in?connectionId=$CONNECTION_ID&appToken=%7B%7Bcredentials.appToken%7D%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appToken": "{{credentials.appToken}}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kIS/latest/actions/sign-in?${params}`, {
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
| `appToken` | string | yes | KIS app token from the connection. Default: `{{credentials.appToken}}`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native KIS API returns.

## Native endpoint

Through the native KIS API, this operation is `POST /api_access_auth/sign_in` (base URL `https://api.getkis.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/sign-in.md) for the provider-specific parameters and requirements.

