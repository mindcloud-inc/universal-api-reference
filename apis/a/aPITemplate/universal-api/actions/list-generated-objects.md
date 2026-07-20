# API Template: List Generated Objects

Retrieves generated objects from API Template.

```
GET https://connect.mindcloud.co/v1/universal/aPITemplate/latest/actions/list-generated-objects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a API Template `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aPITemplate/latest/actions/list-generated-objects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aPITemplate/latest/actions/list-generated-objects?${params}`, {
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
| `templateId` | string | no | Filter generated objects by template ID. |
| `transactionRef` | string | no | Filter objects by transaction reference. |
| `transactionType` | string | no | Filter objects by transaction type. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native API Template API returns.

## Native endpoint

Through the native API Template API, this operation is `GET /v2/list-objects` (base URL `https://rest.apitemplate.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-generated-objects.md) for the provider-specific parameters and requirements.

