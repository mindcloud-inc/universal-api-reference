# Honeybadger: Report Deployment

Reports an application deployment to Honeybadger.

```
POST https://connect.mindcloud.co/v1/universal/honeybadger/latest/actions/report-deployment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Honeybadger `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/honeybadger/latest/actions/report-deployment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/honeybadger/latest/actions/report-deployment', {
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
| `deploy.environment` | string | no | Environment name for the deployment notification. |
| `deploy.revision` | string | no | VCS revision or tag being deployed. |
| `deploy.repository` | string | no | HTTPS repository URL for the deployed codebase. |
| `deploy.localUsername` | string | no | User name of the person running the deployment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | Deployment API status value returned by Honeybadger. |

## Native endpoint

Through the native Honeybadger API, this operation is `POST /deploys` (base URL `https://api.honeybadger.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/report-deployment.md) for the provider-specific parameters and requirements.

