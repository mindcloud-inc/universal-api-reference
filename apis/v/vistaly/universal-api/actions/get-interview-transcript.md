# Vistaly: Get Interview Transcript

Retrieves an interview transcript from Vistaly.

```
GET https://connect.mindcloud.co/v1/universal/vistaly/latest/actions/get-interview-transcript
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vistaly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vistaly/latest/actions/get-interview-transcript?connectionId=$CONNECTION_ID&interviewId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "interviewId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vistaly/latest/actions/get-interview-transcript?${params}`, {
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
| `interviewId` | string | yes | The unique identifier for the interview. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Vistaly API returns.

## Native endpoint

Through the native Vistaly API, this operation is `GET /v1/interviews/{interviewId}/transcript` (base URL `https://api.vistaly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-interview-transcript.md) for the provider-specific parameters and requirements.

