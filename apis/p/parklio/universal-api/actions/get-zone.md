# Parklio: Get Zone

Retrieves a zone from Parklio.

```
GET https://connect.mindcloud.co/v1/universal/parklio/latest/actions/get-zone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Parklio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/parklio/latest/actions/get-zone?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/parklio/latest/actions/get-zone?${params}`, {
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
| `id` | number | yes | The Parklio zone ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Parklio API returns.

## Native endpoint

Through the native Parklio API, this operation is `GET /v2/zones/:id` (base URL `https://api.parklio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-zone.md) for the provider-specific parameters and requirements.

