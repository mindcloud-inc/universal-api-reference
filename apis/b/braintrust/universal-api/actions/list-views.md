# Braintrust: List Views

Retrieves views from Braintrust.

```
GET https://connect.mindcloud.co/v1/universal/braintrust/latest/actions/list-views
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Braintrust `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/braintrust/latest/actions/list-views?connectionId=$CONNECTION_ID&limit=25&offset=0&objectType=string&objectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "objectType": "string",
  "objectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/braintrust/latest/actions/list-views?${params}`, {
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
| `objectType` | string | yes | Type of object the view applies to. |
| `objectId` | string | yes | Id of the object the view applies to. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Braintrust API returns.

## Native endpoint

Through the native Braintrust API, this operation is `GET /v1/view` (base URL `https://api.braintrust.dev`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-views.md) for the provider-specific parameters and requirements.

