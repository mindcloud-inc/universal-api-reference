# Eversign: Download Final PDF

Downloads a final document PDF from Eversign.

```
GET https://connect.mindcloud.co/v1/universal/eversign/latest/actions/download-final-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eversign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eversign/latest/actions/download-final-pdf?connectionId=$CONNECTION_ID&documentHash=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentHash": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eversign/latest/actions/download-final-pdf?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentHash` | string | yes |  |
| `urlOnly` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Eversign API returns.

## Native endpoint

Through the native Eversign API, this operation is `GET /download_final_document` (base URL `https://api.eversign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-final-pdf.md) for the provider-specific parameters and requirements.

