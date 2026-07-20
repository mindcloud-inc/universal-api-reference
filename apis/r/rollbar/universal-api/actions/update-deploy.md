# Rollbar: Update Deploy

Updates an existing deploy in Rollbar.

```
PUT https://connect.mindcloud.co/v1/universal/rollbar/latest/actions/update-deploy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rollbar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rollbar/latest/actions/update-deploy" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "deployId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rollbar/latest/actions/update-deploy', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "deployId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deployId` | number | yes | Rollbar deploy identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "err": 1,
      "result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `err` | number |  |
| `result` | object |  |

## Native endpoint

Through the native Rollbar API, this operation is `PATCH /deploy/:deployId` (base URL `https://api.rollbar.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-deploy.md) for the provider-specific parameters and requirements.

