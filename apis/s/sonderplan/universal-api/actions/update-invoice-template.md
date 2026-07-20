# Sonderplan: Update Invoice Template



```
PUT https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/update-invoice-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sonderplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/update-invoice-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/update-invoice-template', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | Invoice template payload. |
| `id` | string | yes | Invoice template ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Sonderplan API, this operation is `PUT /invoice-template` (base URL `https://api.sonderplan.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-invoice-template.md) for the provider-specific parameters and requirements.

