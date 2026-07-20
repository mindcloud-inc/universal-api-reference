# Agilite: Generate Number

Generates a unique number in Agilite by profile key.

```
POST https://connect.mindcloud.co/v1/universal/agilite/latest/actions/generate-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agilite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/agilite/latest/actions/generate-number" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "profileKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agilite/latest/actions/generate-number', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "profileKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `profileKey` | string | yes | Numbering profile key to generate from. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "number": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `number` | string | Generated number returned by Agilit-e. |

## Native endpoint

Through the native Agilite API, this operation is `POST /numbering/generate` (base URL `https://api.agilite.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-number.md) for the provider-specific parameters and requirements.

