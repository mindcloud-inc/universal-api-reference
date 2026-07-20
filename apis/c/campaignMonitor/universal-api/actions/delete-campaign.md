# Campaign Monitor: Delete Campaign

Deletes an existing campaign from Campaign Monitor.

```
DELETE https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/delete-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campaign Monitor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/delete-campaign?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/delete-campaign?${params}`, {
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
| `campaignId` | string | yes | Campaign Monitor campaign identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Empty string on success because Campaign Monitor returns HTTP 200 OK with no response body for campaign deletes. |

## Native endpoint

Through the native Campaign Monitor API, this operation is `DELETE /campaigns/:campaignId.json` (base URL `https://api.createsend.com/api/v3.3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-campaign.md) for the provider-specific parameters and requirements.

