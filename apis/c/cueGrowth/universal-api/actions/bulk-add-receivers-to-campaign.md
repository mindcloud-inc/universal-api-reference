# CueGrowth: Bulk Add Receivers To Campaign



```
PUT https://connect.mindcloud.co/v1/universal/cueGrowth/latest/actions/bulk-add-receivers-to-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CueGrowth `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cueGrowth/latest/actions/bulk-add-receivers-to-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cueGrowth/latest/actions/bulk-add-receivers-to-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data[]` | array<object> | yes | Array of receivers to add to the campaign. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": {
        "loc": [
          [
            "string"
          ]
        ],
        "msg": "string",
        "type": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error.loc[]` | array<string> |  |
| `error.msg` | string |  |
| `error.type` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native CueGrowth API, this operation is `POST /actions/bulk/add_receiver_to_campaign` (base URL `https://api.cuegrowth.ai/public/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-add-receivers-to-campaign.md) for the provider-specific parameters and requirements.

