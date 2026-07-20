# Pipedream: Get workspaces's subscriptions

Retrieves subscriptions for a workspace from Pipedream.

```
GET https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/get-workspaces-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/get-workspaces-subscriptions?connectionId=$CONNECTION_ID&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/get-workspaces-subscriptions?${params}`, {
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
| `workspaceId` | string | yes | The workspace identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "emitterId": "string",
      "eventName": "Ava Chen",
      "id": "string",
      "listenerId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `emitterId` | string |  |
| `eventName` | string |  |
| `id` | string |  |
| `listenerId` | string |  |

## Native endpoint

Through the native Pipedream API, this operation is `GET /workspaces/{org_id}/subscriptions` (base URL `https://api.pipedream.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspaces-subscriptions.md) for the provider-specific parameters and requirements.

