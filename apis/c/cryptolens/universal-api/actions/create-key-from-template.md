# Cryptolens: Create Key From Template

Creates a license key from a template in Cryptolens.

```
POST https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/create-key-from-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cryptolens `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/create-key-from-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "licenseTemplateId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/create-key-from-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "licenseTemplateId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `licenseTemplateId` | number | yes | The license template id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "key": "string",
      "rawResponse": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `key` | string | Create Key From Template response field `key` from Cryptolens docs example. |
| `rawResponse` | string | Create Key From Template response field `rawResponse` from Cryptolens docs example. |

## Native endpoint

Through the native Cryptolens API, this operation is `GET /api/key/CreateKeyFromTemplate` (base URL `https://api.cryptolens.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-key-from-template.md) for the provider-specific parameters and requirements.

