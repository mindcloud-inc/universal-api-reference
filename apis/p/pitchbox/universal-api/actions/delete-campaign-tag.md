# Pitchbox: Delete Campaign Tag



```
DELETE https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/delete-campaign-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pitchbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/delete-campaign-tag?connectionId=$CONNECTION_ID&campaignId=1&tagId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "1",
  "tagId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/delete-campaign-tag?${params}`, {
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
| `campaignId` | number | yes | The campaign id. |
| `tagId` | number | yes | The id of the tag to remove from the campaign. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pitchbox API returns.

## Native endpoint

Through the native Pitchbox API, this operation is `DELETE /api/campaigns/:campaignId/tags/:tagId` (base URL `https://apiv2.pitchbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-campaign-tag.md) for the provider-specific parameters and requirements.

