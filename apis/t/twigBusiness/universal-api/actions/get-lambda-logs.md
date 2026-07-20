# Twig Business: Get Lambda Logs



```
GET https://connect.mindcloud.co/v1/universal/twigBusiness/latest/actions/get-lambda-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twig Business `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twigBusiness/latest/actions/get-lambda-logs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twigBusiness/latest/actions/get-lambda-logs?${params}`, {
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
| `processId` | string | no | Process identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Twig Business API returns.

## Native endpoint

Through the native Twig Business API, this operation is `GET lambda-logs` (base URL `https://app.twig.so/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lambda-logs.md) for the provider-specific parameters and requirements.

