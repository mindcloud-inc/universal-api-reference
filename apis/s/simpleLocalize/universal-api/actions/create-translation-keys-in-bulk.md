# SimpleLocalize: Create Translation Keys in Bulk

Creates translation keys in bulk in SimpleLocalize.

```
POST https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/create-translation-keys-in-bulk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleLocalize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/create-translation-keys-in-bulk" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/create-translation-keys-in-bulk', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `translationKeys[]` | array<object> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "failures": [
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
| `failures` | array<object> |  |

## Native endpoint

Through the native SimpleLocalize API, this operation is `POST /api/v1/translation-keys/bulk` (base URL `https://api.simplelocalize.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-translation-keys-in-bulk.md) for the provider-specific parameters and requirements.

