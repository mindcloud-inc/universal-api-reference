# fynk: Update Document Party

Updates a document party in fynk.

```
PUT https://connect.mindcloud.co/v1/universal/fynk/latest/actions/update-document-party
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a fynk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fynk/latest/actions/update-document-party" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fynk/latest/actions/update-document-party', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `document` | string | no | Document UUID. Default: `25c718b2-be8b-44e7-858f-3152e7380022`. |
| `entity_name` | string | no | Updated party entity name. Default: `MindCloud Counterparty GmbH`. |
| `party` | string | no | Party UUID. Default: `ebf42312-db03-44f8-b25f-eba6c51a4a26`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native fynk API, this operation is `PUT /documents/:document/parties/:party` (base URL `https://app.fynk.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-document-party.md) for the provider-specific parameters and requirements.

