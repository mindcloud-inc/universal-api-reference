# Arize AX: Get a Space

Retrieves a space from Arize AX.

```
GET https://connect.mindcloud.co/v1/universal/arizeAX/latest/actions/get-a-space
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Arize AX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/arizeAX/latest/actions/get-a-space?connectionId=$CONNECTION_ID&spaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "spaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/arizeAX/latest/actions/get-a-space?${params}`, {
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
| `spaceId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Arize AX API returns.

## Native endpoint

Through the native Arize AX API, this operation is `GET /v2/spaces/:spaceId` (base URL `https://api.arize.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-space.md) for the provider-specific parameters and requirements.

