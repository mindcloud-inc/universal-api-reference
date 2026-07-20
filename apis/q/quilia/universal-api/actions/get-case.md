# Quilia: Get Case



```
GET https://connect.mindcloud.co/v1/universal/quilia/latest/actions/get-case
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quilia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quilia/latest/actions/get-case?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quilia/latest/actions/get-case?${params}`, {
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
| `id` | string | yes | The unique identifier of the case to retrieve |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Quilia API returns.

## Native endpoint

Through the native Quilia API, this operation is `GET cases/:id` (base URL `https://api.quilia.dev/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-case.md) for the provider-specific parameters and requirements.

