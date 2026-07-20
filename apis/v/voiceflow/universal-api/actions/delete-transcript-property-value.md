# Voiceflow: Delete Transcript Property Value

Deletes a transcript property value from Voiceflow.

```
DELETE https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/delete-transcript-property-value
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voiceflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/delete-transcript-property-value?connectionId=$CONNECTION_ID&transcriptId=69c58349e2e653adc0dbddc5&propertyId=69c5834ee2e653adc0dbddd2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transcriptId": "69c58349e2e653adc0dbddc5",
  "propertyId": "69c5834ee2e653adc0dbddd2"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/delete-transcript-property-value?${params}`, {
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
| `transcriptId` | string | yes | ID of the transcript to target. Example: `69c58349e2e653adc0dbddc5`. |
| `propertyId` | string | yes | ID of the property to target. Example: `69c5834ee2e653adc0dbddd2`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Voiceflow API returns.

## Native endpoint

Through the native Voiceflow API, this operation is `DELETE https://analytics-api.voiceflow.com/v1/transcript-property-value/transcript/:transcriptId/property/:propertyId` (base URL `https://general-runtime.voiceflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-transcript-property-value.md) for the provider-specific parameters and requirements.

