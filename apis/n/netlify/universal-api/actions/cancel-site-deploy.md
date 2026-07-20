# Netlify: Cancel Site Deploy



```
PUT https://connect.mindcloud.co/v1/universal/netlify/latest/actions/cancel-site-deploy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Netlify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/netlify/latest/actions/cancel-site-deploy" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "deployId": "69aac8135e01826d281456d7"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netlify/latest/actions/cancel-site-deploy', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "deployId": "69aac8135e01826d281456d7"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deployId` | string | yes | Example: `69aac8135e01826d281456d7`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "context": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deployUrl": "https://example.com",
      "id": "string",
      "manualDeploy": true,
      "name": "Ava Chen",
      "siteId": "string",
      "state": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `context` | string | Deploy context |
| `createdAt` | date | Creation timestamp |
| `deployUrl` | string | Deploy URL |
| `id` | string | Deploy ID |
| `manualDeploy` | boolean | Whether the deploy was created manually |
| `name` | string | Deploy name |
| `siteId` | string | Site ID |
| `state` | string | Deploy state |
| `updatedAt` | date | Last update timestamp |
| `url` | string | Published URL |

## Native endpoint

Through the native Netlify API, this operation is `POST /deploys/:deploy_id/cancel` (base URL `https://api.netlify.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-site-deploy.md) for the provider-specific parameters and requirements.

