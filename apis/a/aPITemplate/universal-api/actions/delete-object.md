# API Template: Delete Object

Deletes an existing generated object from API Template.

```
DELETE https://connect.mindcloud.co/v1/universal/aPITemplate/latest/actions/delete-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a API Template `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/aPITemplate/latest/actions/delete-object?connectionId=$CONNECTION_ID&transactionRef=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transactionRef": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aPITemplate/latest/actions/delete-object?${params}`, {
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
| `transactionRef` | string | yes | Transaction reference of the object to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native API Template API returns.

## Native endpoint

Through the native API Template API, this operation is `GET /v2/delete-object` (base URL `https://rest.apitemplate.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-object.md) for the provider-specific parameters and requirements.

