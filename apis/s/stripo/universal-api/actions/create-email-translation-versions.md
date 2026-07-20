# Stripo: Create Email Translation Versions

Creates translation versions for an email in Stripo.

```
POST https://connect.mindcloud.co/v1/universal/stripo/latest/actions/create-email-translation-versions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stripo/latest/actions/create-email-translation-versions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "languages[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stripo/latest/actions/create-email-translation-versions', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "languages[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The email ID. |
| `languages[]` | array<string> | yes | Language codes for translation versions. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "languages": [
        "string"
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `languages` | array<string> | Language codes requested for email translation versions. |
| `success` | boolean | 200 OK confirmation that translation versions were requested. |

## Native endpoint

Through the native Stripo API, this operation is `POST /emails/:id/translation-versions` (base URL `https://my.stripo.email/emailgeneration/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-email-translation-versions.md) for the provider-specific parameters and requirements.

