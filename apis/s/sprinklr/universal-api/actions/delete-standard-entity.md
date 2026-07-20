# Sprinklr: Delete Standard Entity

Deletes an existing standard entity from Sprinklr.

```
DELETE https://connect.mindcloud.co/v1/universal/sprinklr/latest/actions/delete-standard-entity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sprinklr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sprinklr/latest/actions/delete-standard-entity?connectionId=$CONNECTION_ID&entityId=string&entityType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entityId": "string",
  "entityType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sprinklr/latest/actions/delete-standard-entity?${params}`, {
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
| `entityId` | string | yes |  |
| `entityType` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sprinklr API returns.

## Native endpoint

Through the native Sprinklr API, this operation is `DELETE api/v2/standard-entity/entity/{entityType}/{entityId}` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-standard-entity.md) for the provider-specific parameters and requirements.

