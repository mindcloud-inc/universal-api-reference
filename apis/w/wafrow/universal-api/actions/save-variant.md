# Wafrow: Save Variant

Creates a saved personalization variant in Wafrow.

```
POST https://connect.mindcloud.co/v1/universal/wafrow/latest/actions/save-variant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wafrow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wafrow/latest/actions/save-variant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wafrow/latest/actions/save-variant', {
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
| `templateId` | string | yes | The Wafrow template UUID to save a personalization preset for. |
| `personalize` | object | no | Layer overrides keyed by template layer name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign` | object | Created Wafrow campaign preset including ids, organization, and template references. |
| `success` | boolean | Whether Wafrow saved the variant successfully. |

## Native endpoint

Through the native Wafrow API, this operation is `POST /storeVariant/:templateID` (base URL `https://wafrow.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/save-variant.md) for the provider-specific parameters and requirements.

