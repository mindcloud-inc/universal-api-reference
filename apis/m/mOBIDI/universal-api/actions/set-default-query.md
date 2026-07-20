# MOBIDI: Set Default Query

Sets the default query in MOBIDI.

```
PUT https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/set-default-query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MOBIDI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/set-default-query" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "queryObject": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/set-default-query', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "queryObject": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `queryObject` | string | yes | Serialized MobidiQuery payload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | boolean | True when the supplied query becomes the default query. |

## Native endpoint

Through the native MOBIDI API, this operation is `POST /MobidiQueryManagerHandler` (base URL `https://servis2.dece.com.tr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-default-query.md) for the provider-specific parameters and requirements.

