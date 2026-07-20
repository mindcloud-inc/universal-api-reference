# Shuffler: Bulk Set Datastore Keys

Creates multiple datastore keys in Shuffler.

```
POST https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/bulk-set-datastore-keys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shuffler `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/bulk-set-datastore-keys" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bulk": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/bulk-set-datastore-keys', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bulk": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bulk` | boolean | yes | Set to true for bulk datastore writes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "keysExisted": [
        "string"
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `keysExisted` | array |  |
| `success` | boolean |  |

## Native endpoint

Through the native Shuffler API, this operation is `POST /v2/datastore` (base URL `https://shuffler.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-set-datastore-keys.md) for the provider-specific parameters and requirements.

