# 1001fx: Create Fake Data

Creates fake test data with 1001fx.

```
POST https://connect.mindcloud.co/v1/universal/fx/latest/actions/create-fake-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 1001fx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fx/latest/actions/create-fake-data" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fx/latest/actions/create-fake-data', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data[]` | array | yes | Array of fake-data definitions to generate. |
| `locale` | string | no | Locale used for generated fake data. |
| `rows` | number | no | Number of fake-data rows to generate. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 1001fx API returns.

## Native endpoint

Through the native 1001fx API, this operation is `POST /data/createfakedata` (base URL `https://api.1001fx.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-fake-data.md) for the provider-specific parameters and requirements.

