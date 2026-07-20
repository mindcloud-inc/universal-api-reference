# Arize AX: Get a Prompt

Retrieves a prompt from Arize AX.

```
GET https://connect.mindcloud.co/v1/universal/arizeAX/latest/actions/get-a-prompt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Arize AX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/arizeAX/latest/actions/get-a-prompt?connectionId=$CONNECTION_ID&promptId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "promptId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/arizeAX/latest/actions/get-a-prompt?${params}`, {
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
| `promptId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Arize AX API returns.

## Native endpoint

Through the native Arize AX API, this operation is `GET /v2/prompts/:promptId` (base URL `https://api.arize.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-prompt.md) for the provider-specific parameters and requirements.

