# OneAll: Relink Identity

Relinks a social identity to another user in OneAll.

```
PUT https://connect.mindcloud.co/v1/universal/oneAll/latest/actions/relink-identity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneAll `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/oneAll/latest/actions/relink-identity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identityToken": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneAll/latest/actions/relink-identity', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "identityToken": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `identityToken` | string | yes | The OneAll identity token. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OneAll API returns.

## Native endpoint

Through the native OneAll API, this operation is `PUT /identities/<identity_token>/link.json` (base URL `https://mindcloudco.api.oneall.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/relink-identity.md) for the provider-specific parameters and requirements.

