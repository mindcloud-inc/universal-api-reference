# deAPI: Get Sample Prompts

Retrieves sample prompts for AI tasks from deAPI.

```
GET https://connect.mindcloud.co/v1/universal/deAPI/latest/actions/get-sample-prompts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a deAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deAPI/latest/actions/get-sample-prompts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deAPI/latest/actions/get-sample-prompts?${params}`, {
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
| `langCode` | string | no | Optional language code for text2speech prompt generation. |
| `topic` | string | no | Optional topic to guide the generated sample prompt. |
| `type` | string | no | Sample prompt type such as text2image or text2speech. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native deAPI API returns.

## Native endpoint

Through the native deAPI API, this operation is `GET /api/v1/client/prompts/samples` (base URL `https://api.deapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sample-prompts.md) for the provider-specific parameters and requirements.

