# Voiceflow: Update Transcript Property

Updates an existing transcript property in Voiceflow.

```
PUT https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/update-transcript-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voiceflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/update-transcript-property" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "propertyId": "69c57fb837fdbf3735905537"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/update-transcript-property', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "propertyId": "69c57fb837fdbf3735905537"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `propertyId` | string | yes | ID of the property to target. Example: `69c57fb837fdbf3735905537`. |
| `name` | string | no | The name of this property. Example: `Wizard Temp Property Updated`. |
| `type` | string | no | The type of value held by this property. Example: `string`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Voiceflow API returns.

## Native endpoint

Through the native Voiceflow API, this operation is `PATCH https://analytics-api.voiceflow.com/v1/transcript-property/:propertyId` (base URL `https://general-runtime.voiceflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-transcript-property.md) for the provider-specific parameters and requirements.

