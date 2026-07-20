# TAYL: Create Tale From Text



```
POST https://connect.mindcloud.co/v1/universal/tAYL/latest/actions/create-tale-from-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TAYL `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tAYL/latest/actions/create-tale-from-text" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "markup": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tAYL/latest/actions/create-tale-from-text', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "markup": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Title for the text-based tale. |
| `markup` | string | yes | HTML markup or rich text content to convert into a tale. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "taleId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `taleId` | string |  |

## Native endpoint

Through the native TAYL API, this operation is `POST /submit` (base URL `https://x.tayl.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tale-from-text.md) for the provider-specific parameters and requirements.

