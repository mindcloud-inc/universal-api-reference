# CraftMyPDF: Retain template versions

Updates retained template versions in CraftMyPDF.

```
PUT https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/retain-template-versions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CraftMyPDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/retain-template-versions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string",
  "versions[]": [
    1
  ],
  "keep": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/retain-template-versions', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string",
    "versions[]": [1],
    "keep": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes |  |
| `versions[]` | array<number> | yes |  |
| `keep` | boolean | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string",
      "templateId": "string",
      "versions": [
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
| `status` | string |  |
| `templateId` | string |  |
| `versions` | array<object> |  |

## Native endpoint

Through the native CraftMyPDF API, this operation is `POST /retain-template-versions` (base URL `https://api.craftmypdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retain-template-versions.md) for the provider-specific parameters and requirements.

