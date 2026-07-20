# Documenso: Create Fields

Creates fields in Documenso.

```
POST https://connect.mindcloud.co/v1/universal/documenso/latest/actions/create-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documenso `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/documenso/latest/actions/create-fields" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "envelopeId": "string",
  "data[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documenso/latest/actions/create-fields', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "envelopeId": "string",
    "data[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `envelopeId` | string | yes |  |
| `data[]` | array<object> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |

## Native endpoint

Through the native Documenso API, this operation is `POST /envelope/field/create-many` (base URL `https://app.documenso.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-fields.md) for the provider-specific parameters and requirements.

