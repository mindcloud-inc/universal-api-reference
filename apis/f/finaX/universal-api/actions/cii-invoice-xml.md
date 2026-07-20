# finaX: CII Invoice Xml

Creates CII invoice XML from JSON in finaX.

```
POST https://connect.mindcloud.co/v1/universal/finaX/latest/actions/cii-invoice-xml
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a finaX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/finaX/latest/actions/cii-invoice-xml" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoice": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/finaX/latest/actions/cii-invoice-xml', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoice": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invoice` | object | yes | Invoice payload to convert to CII XML. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "xml": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `xml` | string | Generated CII XML response. |

## Native endpoint

Through the native finaX API, this operation is `POST /v1/xml/cii/` (base URL `https://api.finax.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cii-invoice-xml.md) for the provider-specific parameters and requirements.

