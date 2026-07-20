# Minelead: Generate Tags



```
POST https://connect.mindcloud.co/v1/universal/minelead/latest/actions/generate-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Minelead `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/minelead/latest/actions/generate-tags" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tags": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/minelead/latest/actions/generate-tags', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tags": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tags` | list<string> | yes | List of tags to generate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companies": [
        "string"
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
| `companies` | array<string> |  |
| `status` | string |  |

## Native endpoint

Through the native Minelead API, this operation is `POST /tags/` (base URL `https://api.minelead.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-tags.md) for the provider-specific parameters and requirements.

