# Happy SMS: Create Document



```
POST https://connect.mindcloud.co/v1/universal/happySMS/latest/actions/create-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Happy SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/happySMS/latest/actions/create-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "resource[]": [
    {
      "label": "name",
      "value": "MindCloud Test Document"
    },
    {
      "label": "_tel",
      "value": "+687999999"
    }
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/happySMS/latest/actions/create-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "resource[]": [{"label":"name","value":"MindCloud Test Document"},{"label":"_tel","value":"+687999999"}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `resource[]` | array<object> | yes | Array of document property objects to create. Default: `[{"label":"name","value":"MindCloud Test Document"},{"label":"_tel","value":"+687999999"}]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "": [
        {
          "key": "string",
          "label": "string",
          "type": "string",
          "value": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `[].key` | string | Generated property key. |
| `[].label` | string | Document property label. |
| `[].type` | string | Document property type. |
| `[].value` | string | Document property value. |

## Native endpoint

Through the native Happy SMS API, this operation is `POST /api/v1/protected/domain/custom-data/documents` (base URL `https://www.api.nc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document.md) for the provider-specific parameters and requirements.

