# Sprinklr: Create Custom Entity

Creates a custom entity in Sprinklr.

```
POST https://connect.mindcloud.co/v1/universal/sprinklr/latest/actions/create-custom-entity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sprinklr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sprinklr/latest/actions/create-custom-entity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "requestBody": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sprinklr/latest/actions/create-custom-entity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "requestBody": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `requestBody` | object | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sprinklr API returns.

## Native endpoint

Through the native Sprinklr API, this operation is `POST api/v2/custom-entity/entity` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-custom-entity.md) for the provider-specific parameters and requirements.

