# SeaX: Get Campaign

Retrieves a campaign from the current SeaX workspace.

```
GET https://connect.mindcloud.co/v1/universal/seaX/latest/actions/get-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seaX/latest/actions/get-campaign?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seaX/latest/actions/get-campaign?${params}`, {
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
| `campaignId` | string | yes | Campaign identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_time": "string",
      "id": "string",
      "message": "string",
      "name": "Ava Chen",
      "status": {},
      "type": {},
      "updated_time": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_time` | string |  |
| `id` | string |  |
| `message` | string |  |
| `name` | string |  |
| `status` | object |  |
| `type` | object |  |
| `updated_time` | string |  |

## Native endpoint

Through the native SeaX API, this operation is `GET /campaigns/{campaign_id}` (base URL `https://seax.seasalt.ai/seax-api/api/v1/workspace/{{credentials.workspaceId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign.md) for the provider-specific parameters and requirements.

