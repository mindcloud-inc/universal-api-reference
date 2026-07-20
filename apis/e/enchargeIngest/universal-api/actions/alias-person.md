# Encharge Ingest: Alias Person



```
PUT https://connect.mindcloud.co/v1/universal/enchargeIngest/latest/actions/alias-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encharge Ingest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/enchargeIngest/latest/actions/alias-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "user": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/enchargeIngest/latest/actions/alias-person', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "user": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `previousUserId` | string | no | Existing userId before the alias change. |
| `previousEmail` | string | no | Existing email before the alias change. |
| `user` | object | yes | JSON object containing the new `email` and/or `userId` values. |

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

Through the native Encharge Ingest API, this operation is `POST /` (base URL `https://ingest.encharge.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/alias-person.md) for the provider-specific parameters and requirements.

