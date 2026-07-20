# Atlas AI Revenue Engine: Update Campaign



```
PUT https://connect.mindcloud.co/v1/universal/atlasAIRevenueEngine/latest/actions/update-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlas AI Revenue Engine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/atlasAIRevenueEngine/latest/actions/update-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/atlasAIRevenueEngine/latest/actions/update-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The campaign ID. |
| `agentTypeName` | string | no | Agent type name. |
| `language` | string | no | Agent language. |
| `name` | string | no | Campaign or agent display name. |
| `postScript` | string | no | Post-script text. |
| `preScript` | string | no | Pre-script text. |
| `voiceId` | string | no | Voice identifier. |
| `model` | string | no | Voice model. |
| `provider` | string | no | Voice provider. |
| `stability` | number | no | Voice stability setting. |
| `similarityBoost` | number | no | Voice similarity boost setting. |
| `backgroundSound` | string | no | Background sound setting. |
| `atlasVoiceId` | string | no | Atlas voice identifier. |
| `pitch` | number | no | Voice pitch setting. |
| `gender` | string | no | Voice gender. |
| `speed` | number | no | Voice speed setting. |
| `slug` | string | no | Campaign slug. |
| `languageBoost` | string | no | Language boost setting. |
| `textNormalizationEnabled` | boolean | no | Whether text normalization is enabled. |
| `region` | string | no | Voice region. |
| `volume` | number | no | Voice volume setting. |
| `fillerInjectionEnabled` | boolean | no | Whether filler injection is enabled. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | no | Optional campaign identifier in the request body. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Atlas AI Revenue Engine API returns.

## Native endpoint

Through the native Atlas AI Revenue Engine API, this operation is `PUT /campaign/:id` (base URL `https://api.youratlas.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-campaign.md) for the provider-specific parameters and requirements.

