# Appzi: Set User Identification

Generates an Appzi user identification settings snippet.

```
PUT https://connect.mindcloud.co/v1/universal/appzi/latest/actions/set-user-identification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appzi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/appzi/latest/actions/set-user-identification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appzi/latest/actions/set-user-identification', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | yes | Stable user identifier inserted into the generated Appzi tracking snippet. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Appzi API returns.

## Native endpoint

Through the native Appzi API, this operation is `GET https://docs.appzi.io/integration/add-data/` (base URL `https://api.appzi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-user-identification.md) for the provider-specific parameters and requirements.

