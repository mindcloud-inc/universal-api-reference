# Pitchbox: Add Campaign Tag



```
POST https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/add-campaign-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pitchbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/add-campaign-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": 1,
  "tag": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/add-campaign-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": 1,
    "tag": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | number | yes | The campaign id. |
| `tag` | number | yes | The id of the tag to attach to the campaign. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "tag": {
        "color": "string",
        "id": 1,
        "name": "Ava Chen",
        "type": "string"
      },
      "taggedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `tag.color` | string |  |
| `tag.id` | number |  |
| `tag.name` | string |  |
| `tag.type` | string |  |
| `taggedAt` | date |  |

## Native endpoint

Through the native Pitchbox API, this operation is `POST /api/campaigns/:campaignId/tags` (base URL `https://apiv2.pitchbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-campaign-tag.md) for the provider-specific parameters and requirements.

