# elmah.io: Create Deployment

Creates a new deployment in elmah.io.

```
POST https://connect.mindcloud.co/v1/universal/elmahio/latest/actions/create-deployment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a elmah.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/elmahio/latest/actions/create-deployment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "version": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/elmahio/latest/actions/create-deployment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "version": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `logId` | string | no | Attach the deployment to a single log only. |
| `version` | string | yes | The version number of this deployment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "location": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `location` | string |  |

## Native endpoint

Through the native elmah.io API, this operation is `POST /v3/deployments` (base URL `https://api.elmah.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-deployment.md) for the provider-specific parameters and requirements.

