# Eledo: Generate PDF

Generates a PDF from a template in Eledo.

```
POST https://connect.mindcloud.co/v1/universal/eledo/latest/actions/generate-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eledo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eledo/latest/actions/generate-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eledo/latest/actions/generate-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes |  |
| `templateVersion` | number | no |  |
| `file` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[]` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Eledo API, this operation is `POST /Generate` (base URL `https://eledo.online/api/RESTv1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-pdf.md) for the provider-specific parameters and requirements.

