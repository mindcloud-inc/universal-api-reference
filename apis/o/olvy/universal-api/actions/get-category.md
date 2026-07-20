# Olvy: Get Category

Retrieves category details from Olvy.

```
GET https://connect.mindcloud.co/v1/universal/olvy/latest/actions/get-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Olvy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/olvy/latest/actions/get-category?connectionId=$CONNECTION_ID&variables.id=4e4ff687-fb2d-40cb-9abd-146505f1013c" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.id": "4e4ff687-fb2d-40cb-9abd-146505f1013c"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/olvy/latest/actions/get-category?${params}`, {
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
| `variables.id` | string | yes | Category id to retrieve. Example: `4e4ff687-fb2d-40cb-9abd-146505f1013c`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Olvy API returns.

## Native endpoint

Through the native Olvy API, this operation is `POST /` (base URL `https://app.olvy.co/api/v2/graphql`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-category.md) for the provider-specific parameters and requirements.

