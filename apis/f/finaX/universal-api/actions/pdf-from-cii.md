# finaX: PDF From CII

Creates a ZUGFeRD PDF from CII XML in finaX.

```
POST https://connect.mindcloud.co/v1/universal/finaX/latest/actions/pdf-from-cii
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a finaX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/finaX/latest/actions/pdf-from-cii" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "xml": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/finaX/latest/actions/pdf-from-cii', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "xml": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `xml` | string | yes | CII XML payload. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native finaX API returns.

## Native endpoint

Through the native finaX API, this operation is `POST /v1/pdf/cii/` (base URL `https://api.finax.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/pdf-from-cii.md) for the provider-specific parameters and requirements.

