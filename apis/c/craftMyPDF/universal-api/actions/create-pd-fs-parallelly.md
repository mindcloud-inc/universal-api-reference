# CraftMyPDF: Create PDFs parallelly

Creates multiple PDFs in parallel in CraftMyPDF.

```
POST https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/create-pd-fs-parallelly
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CraftMyPDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/create-pd-fs-parallelly" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "requests[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/create-pd-fs-parallelly', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "requests[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `requests[]` | array<object> | yes |  |
| `merge` | boolean | no |  |
| `mergeExpiration` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results` | array<object> |  |
| `status` | string |  |

## Native endpoint

Through the native CraftMyPDF API, this operation is `POST /create-parallel` (base URL `https://api.craftmypdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pd-fs-parallelly.md) for the provider-specific parameters and requirements.

