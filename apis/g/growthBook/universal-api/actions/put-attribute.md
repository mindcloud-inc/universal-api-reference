# GrowthBook: Update an attribute

Updates an existing attribute in GrowthBook.

```
PUT https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/put-attribute
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/put-attribute" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "property": "sampleAttribute"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/put-attribute', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "property": "sampleAttribute"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `property` | string | yes | The attribute property Default: `sampleAttribute`. |
| `datatype` | string | no | The attribute datatype |
| `description` | string | no | The description of the new attribute |
| `archived` | boolean | no | The attribute is archived |
| `hashAttribute` | boolean | no | Shall the attribute be hashed |
| `enum` | string | no |  |
| `format` | string | no | The attribute's format |
| `projects` | list<string> | no |  |
| `tags` | list<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attribute": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attribute` | object |  |

## Native endpoint

Through the native GrowthBook API, this operation is `PUT /attributes/:property` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/put-attribute.md) for the provider-specific parameters and requirements.

