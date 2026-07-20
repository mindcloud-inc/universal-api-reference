# snapADDY: Get Participant Attachment



```
GET https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/get-participant-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a snapADDY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/get-participant-attachment?connectionId=$CONNECTION_ID&questionnaireId=string&participantId=string&attachmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "questionnaireId": "string",
  "participantId": "string",
  "attachmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/get-participant-attachment?${params}`, {
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
| `questionnaireId` | string | yes | Questionnaire identifier |
| `participantId` | string | yes | Participant identifier |
| `attachmentId` | string | yes | Attachment identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string |  |

## Native endpoint

Through the native snapADDY API, this operation is `GET /visitreport/v1/attachment/:questionnaireId/:participantId/:attachmentId` (base URL `https://api.snapaddy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-participant-attachment.md) for the provider-specific parameters and requirements.

