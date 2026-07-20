# elmah.io: Get Deployment

Retrieves a deployment from elmah.io.

```
GET https://connect.mindcloud.co/v1/universal/elmahio/latest/actions/get-deployment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a elmah.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/elmahio/latest/actions/get-deployment?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/elmahio/latest/actions/get-deployment?${params}`, {
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
| `id` | string | yes | The ID of the deployment to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "string",
      "createdBy": "string",
      "id": "string",
      "logId": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | string |  |
| `createdBy` | string |  |
| `id` | string |  |
| `logId` | string |  |
| `version` | string |  |

## Native endpoint

Through the native elmah.io API, this operation is `GET /v3/deployments/:id` (base URL `https://api.elmah.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-deployment.md) for the provider-specific parameters and requirements.

