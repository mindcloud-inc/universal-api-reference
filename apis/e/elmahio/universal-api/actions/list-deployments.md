# elmah.io: List Deployments

Retrieves deployments from elmah.io.

```
GET https://connect.mindcloud.co/v1/universal/elmahio/latest/actions/list-deployments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a elmah.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/elmahio/latest/actions/list-deployments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/elmahio/latest/actions/list-deployments?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "description": "string",
      "id": "string",
      "logId": "string",
      "userEmail": "ava@example.com",
      "userName": "Ava Chen",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date | When this deployment was created. |
| `createdBy` | string | The elmah.io user ID that created this deployment. |
| `description` | string | Description of this deployment in markdown or plain text. |
| `id` | string | The ID of this deployment. |
| `logId` | string | The log ID when the deployment is attached to a single log. |
| `userEmail` | string | The email of the person responsible for creating this deployment. |
| `userName` | string | The name of the person responsible for creating this deployment. |
| `version` | string | The version number of this deployment. |

## Native endpoint

Through the native elmah.io API, this operation is `GET /v3/deployments` (base URL `https://api.elmah.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-deployments.md) for the provider-specific parameters and requirements.

