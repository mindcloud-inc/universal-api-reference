# Svix: Delete Endpoint

Deletes an endpoint from Svix.

```
DELETE https://connect.mindcloud.co/v1/universal/svix/latest/actions/delete-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Svix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/svix/latest/actions/delete-endpoint?connectionId=$CONNECTION_ID&appId=string&endpointId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string",
  "endpointId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/svix/latest/actions/delete-endpoint?${params}`, {
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
| `appId` | string | yes | The application's ID or UID. |
| `endpointId` | string | yes | The endpoint's ID or UID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Svix API, this operation is `DELETE /api/v1/app/{app_id}/endpoint/{endpoint_id}` (base URL `https://api.us.svix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-endpoint.md) for the provider-specific parameters and requirements.

