# Stripo: Generate Email

Generates an email in Stripo from external source data.

```
POST https://connect.mindcloud.co/v1/universal/stripo/latest/actions/generate-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stripo/latest/actions/generate-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dataSources[]": [
    {}
  ],
  "templateId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stripo/latest/actions/generate-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dataSources[]": [{}],
    "templateId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dataSources[]` | array<object> | yes | Data sources for generation. Accepts multiple values as an array. |
| `emailId` | number | no | Existing email ID to override. |
| `emailName` | string | no | Name for the generated email. |
| `folderId` | number | no | Folder ID for the generated email. |
| `preheader` | string | no | Email preheader. |
| `templateId` | number | yes | Template with the auto-generated area. |
| `title` | string | no | Email title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Generated email ID. |
| `name` | string | Generated email name. |

## Native endpoint

Through the native Stripo API, this operation is `POST /email` (base URL `https://my.stripo.email/emailgeneration/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-email.md) for the provider-specific parameters and requirements.

