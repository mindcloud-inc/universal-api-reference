# GrowthBook: Create a new attribute

Creates a new attribute in GrowthBook.

```
POST https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-attribute
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-attribute" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "property": "sampleAttribute",
  "datatype": "sample"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-attribute', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "property": "sampleAttribute",
    "datatype": "sample"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `property` | string | yes | The attribute property Default: `sampleAttribute`. |
| `datatype` | string | yes | The attribute datatype Default: `sample`. |
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

Through the native GrowthBook API, this operation is `POST /attributes` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-attribute.md) for the provider-specific parameters and requirements.

