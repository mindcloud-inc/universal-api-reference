# Dialpad: Get Call AI Recap

Retrieves an AI recap for a Dialpad call.

```
GET https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/get-call-ai-recap
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dialpad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/get-call-ai-recap?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/get-call-ai-recap?${params}`, {
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
| `id` | number | yes | The call's id. |
| `summary_format` | string | no | The format of the summary to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionItems": [
        {}
      ],
      "callId": "string",
      "dateCreated": 1,
      "dateModified": 1,
      "disposition": {},
      "isInternalCall": true,
      "purposes": [
        {}
      ],
      "source": "string",
      "summary": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionItems` | array<object> | Action items extracted from the call. |
| `callId` | string | The ID of the call for which the AI recap was generated. |
| `dateCreated` | number | When the AI recap was created, in milliseconds. |
| `dateModified` | number | When the AI recap was last modified, in milliseconds. |
| `disposition` | object | Disposition content for the call. |
| `isInternalCall` | boolean | Whether the call was internal. |
| `purposes` | array<object> | Purpose items extracted from the call. |
| `source` | string | The language model source. |
| `summary` | object | The summary content in the requested format. |

## Native endpoint

Through the native Dialpad API, this operation is `GET /call/:id/ai_recap` (base URL `https://dialpad.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-call-ai-recap.md) for the provider-specific parameters and requirements.

