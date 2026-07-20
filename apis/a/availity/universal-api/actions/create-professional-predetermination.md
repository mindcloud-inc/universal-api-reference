# Availity: Create Professional Predetermination

Creates a professional predetermination in Availity.

```
POST https://connect.mindcloud.co/v1/universal/availity/latest/actions/create-professional-predetermination
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Availity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/availity/latest/actions/create-professional-predetermination" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/availity/latest/actions/create-professional-predetermination', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `professionalClaim` | object | no | PCE 1.0 professional claim predetermination request body. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Availity API returns.

## Native endpoint

Through the native Availity API, this operation is `POST /availity/v1/professional-claims` (base URL `https://api.availity.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-professional-predetermination.md) for the provider-specific parameters and requirements.

