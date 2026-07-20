# Dribbble: Create Shot



```
POST https://connect.mindcloud.co/v1/universal/dribbble/latest/actions/create-shot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dribbble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dribbble/latest/actions/create-shot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "image": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dribbble/latest/actions/create-shot', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "image": "string",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `image` | file | yes | The shot image file. |
| `title` | string | yes |  |
| `description` | string | no |  |
| `lowProfile` | boolean | no |  |
| `reboundSourceId` | number | no |  |
| `scheduledFor` | date | no |  |
| `tags[]` | array<string> | no |  |
| `teamId` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dribbble API returns.

## Native endpoint

Through the native Dribbble API, this operation is `POST /shots` (base URL `https://api.dribbble.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-shot.md) for the provider-specific parameters and requirements.

