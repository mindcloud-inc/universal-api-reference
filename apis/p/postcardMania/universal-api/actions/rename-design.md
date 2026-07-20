# PostcardMania: Rename Design

Updates an existing design in PostcardMania.

```
PUT https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/rename-design
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostcardMania `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/rename-design" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/rename-design', {
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
| `designID` | string | no | The design identifier to update. |
| `friendlyName` | string | no | New design name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "designID": 1,
      "friendlyName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `designID` | number | Updated design identifier. |
| `friendlyName` | string | Updated design name. |

## Native endpoint

Through the native PostcardMania API, this operation is `PUT /design/{{designID}}` (base URL `https://v3.pcmintegrations.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rename-design.md) for the provider-specific parameters and requirements.

