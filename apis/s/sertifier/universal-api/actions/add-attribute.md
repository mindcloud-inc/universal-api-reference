# Sertifier: Add Attribute

Creates a new attribute in Sertifier.

```
POST https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/add-attribute
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sertifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/add-attribute" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "type": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/add-attribute', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "type": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Internal title for the attribute. |
| `type` | number | yes | Attribute value type: 1 text, 2 date, 3 number. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native Sertifier API, this operation is `POST /attribute` (base URL `https://b2b.sertifier.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-attribute.md) for the provider-specific parameters and requirements.

