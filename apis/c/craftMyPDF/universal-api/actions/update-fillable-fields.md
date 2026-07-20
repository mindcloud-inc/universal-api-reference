# CraftMyPDF: Update fillable fields

Updates fillable PDF fields in CraftMyPDF.

```
PUT https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/update-fillable-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CraftMyPDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/update-fillable-fields" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com",
  "fields[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/update-fillable-fields', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com",
    "fields[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes |  |
| `fields[]` | array<object> | yes |  |
| `fields[].id` | string | no |  |
| `fields[].value` | string | no |  |
| `fields[].readOnly` | boolean | no |  |
| `fields[].fontSize` | number | no |  |
| `expiration` | number | no |  |
| `outputFile` | string | no |  |
| `cloudStorage` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fieldStatuses": [
        {}
      ],
      "file": "string",
      "status": "string",
      "transactionRef": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fieldStatuses` | array<object> |  |
| `file` | string |  |
| `status` | string |  |
| `transactionRef` | string |  |

## Native endpoint

Through the native CraftMyPDF API, this operation is `POST /update-pdf-fields` (base URL `https://api.craftmypdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-fillable-fields.md) for the provider-specific parameters and requirements.

