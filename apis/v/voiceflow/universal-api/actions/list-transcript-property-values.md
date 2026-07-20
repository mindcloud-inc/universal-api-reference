# Voiceflow: List Transcript Property Values

Retrieves transcript property values from Voiceflow.

```
GET https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/list-transcript-property-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voiceflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/list-transcript-property-values?connectionId=$CONNECTION_ID&transcriptId=69c5805ff9294436f0b75ee0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transcriptId": "69c5805ff9294436f0b75ee0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/list-transcript-property-values?${params}`, {
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
| `transcriptId` | string | yes | ID of the transcript to target. Example: `69c5805ff9294436f0b75ee0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "propertyValues": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "metadata": {},
          "propertyID": "string",
          "transcriptID": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "value": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `propertyValues` | array<object> | Property values associated with the transcript. |
| `propertyValues[].createdAt` | date | When the property value was created. |
| `propertyValues[].metadata` | object | Optional metadata attached to the property value. |
| `propertyValues[].propertyID` | string | ID of the transcript property. |
| `propertyValues[].transcriptID` | string | ID of the transcript. |
| `propertyValues[].updatedAt` | date | When the property value was last updated. |
| `propertyValues[].value` | string | Stored property value. |

## Native endpoint

Through the native Voiceflow API, this operation is `GET https://analytics-api.voiceflow.com/v1/transcript-property-value/transcript/:transcriptId` (base URL `https://general-runtime.voiceflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-transcript-property-values.md) for the provider-specific parameters and requirements.

