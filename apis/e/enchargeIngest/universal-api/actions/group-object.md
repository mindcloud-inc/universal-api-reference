# Encharge Ingest: Group Object



```
POST https://connect.mindcloud.co/v1/universal/enchargeIngest/latest/actions/group-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encharge Ingest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/enchargeIngest/latest/actions/group-object" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "objectType": "string",
  "properties": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/enchargeIngest/latest/actions/group-object', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "objectType": "string",
    "properties": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `objectType` | string | yes | Name of the custom object type to create or update, for example `company`. |
| `properties` | object | yes | JSON object with custom object fields. Include `id` or `externalId` when updating an existing object. |
| `user` | object | no | Optional JSON object containing `email` or `userId` when you want to associate the object with a person. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |

## Native endpoint

Through the native Encharge Ingest API, this operation is `POST /` (base URL `https://ingest.encharge.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/group-object.md) for the provider-specific parameters and requirements.

