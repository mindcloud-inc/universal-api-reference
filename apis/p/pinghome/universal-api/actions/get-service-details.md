# Pinghome: Get Service Details

Retrieves service details from Pinghome.

```
GET https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/get-service-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinghome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/get-service-details?connectionId=$CONNECTION_ID&id=b74ca3ec-c0da-49b3-84ff-1d113b165d70" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "b74ca3ec-c0da-49b3-84ff-1d113b165d70"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/get-service-details?${params}`, {
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
| `id` | string | yes | The team id whose services should be returned. Example: `b74ca3ec-c0da-49b3-84ff-1d113b165d70`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pinghome API returns.

## Native endpoint

Through the native Pinghome API, this operation is `GET /resource-query/v1/team-service/:id` (base URL `https://api.pinghome.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-service-details.md) for the provider-specific parameters and requirements.

