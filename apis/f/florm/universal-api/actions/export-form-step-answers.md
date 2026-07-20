# Florm: Export Form Step Answers

Creates an export task for Florm form step answers.

```
POST https://connect.mindcloud.co/v1/universal/florm/latest/actions/export-form-step-answers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Florm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/florm/latest/actions/export-form-step-answers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string",
  "stepId": 1,
  "formGuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/florm/latest/actions/export-form-step-answers', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string",
    "stepId": 1,
    "formGuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | yes | Export file type. |
| `stepId` | number | yes | Numeric Florm step identifier. |
| `formGuid` | string | yes | GUID of the Florm form to export answers for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "resultString": "string",
      "status": "string",
      "taskGuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `resultString` | string | Provider result string when available. |
| `status` | string | Current export task status. |
| `taskGuid` | string | GUID of the created export task. |

## Native endpoint

Through the native Florm API, this operation is `POST /v1/export/form/step` (base URL `https://api.florm.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-form-step-answers.md) for the provider-specific parameters and requirements.

