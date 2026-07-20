# Shuffler: Set Datastore Key

Creates a datastore key in Shuffler.

```
POST https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/set-datastore-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shuffler `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/set-datastore-key" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "key": "string",
  "orgId": "string",
  "value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/set-datastore-key', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "key": "string",
    "orgId": "string",
    "value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `category` | string | no | Optional datastore category. |
| `key` | string | yes | Datastore key. |
| `orgId` | string | yes | Org Id path parameter. |
| `value` | string | yes | Datastore value. |

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

Through the native Shuffler API, this operation is `POST /orgs/{orgId}/set_cache` (base URL `https://shuffler.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-datastore-key.md) for the provider-specific parameters and requirements.

