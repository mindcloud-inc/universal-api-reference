# Resco Cloud: Update Multiple Records

Updates multiple records in Resco Cloud.

```
PUT https://connect.mindcloud.co/v1/universal/rescoCloud/latest/actions/update-multiple-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Resco Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rescoCloud/latest/actions/update-multiple-records" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "rawBody": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rescoCloud/latest/actions/update-multiple-records', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "rawBody": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `rawBody` | string | yes | XML Entities body for the Resco UpdateMultiple request. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `create` | boolean | no | When true, Resco creates records that do not already exist. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Resco Cloud API returns.

## Native endpoint

Through the native Resco Cloud API, this operation is `POST /UpdateMultiple` (base URL `https://{{credentials.organization}}.app.resco.net/rest/v1/data`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-multiple-records.md) for the provider-specific parameters and requirements.

