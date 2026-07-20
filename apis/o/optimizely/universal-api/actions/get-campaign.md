# Optimizely: Get Campaign

Retrieves campaign details from the Optimizely API.

```
GET https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/get-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Optimizely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/get-campaign?connectionId=$CONNECTION_ID&campaignId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/get-campaign?${params}`, {
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
| `campaignId` | string | yes | The campaign id. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "created": "string",
      "description": "string",
      "id": 1,
      "lastModified": "string",
      "name": "Ava Chen",
      "projectId": 1,
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `created` | string |  |
| `description` | string |  |
| `id` | number |  |
| `lastModified` | string |  |
| `name` | string |  |
| `projectId` | number |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Optimizely API, this operation is `GET /campaigns/{campaignId}` (base URL `https://api.optimizely.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign.md) for the provider-specific parameters and requirements.

