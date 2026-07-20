# Basalt: List Prompts

Retrieves a list of prompts from Basalt.

```
GET https://connect.mindcloud.co/v1/universal/basalt/latest/actions/list-prompts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Basalt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/basalt/latest/actions/list-prompts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/basalt/latest/actions/list-prompts?${params}`, {
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
| `featureSlug` | string | no | Filter prompts by feature slug. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Basalt API returns.

## Native endpoint

Through the native Basalt API, this operation is `GET /prompts` (base URL `https://api.getbasalt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-prompts.md) for the provider-specific parameters and requirements.

