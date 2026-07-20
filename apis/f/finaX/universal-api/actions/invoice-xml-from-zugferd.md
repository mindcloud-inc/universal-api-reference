# finaX: Invoice XML From ZUGFeRD

Retrieves invoice XML from a ZUGFeRD PDF in finaX.

```
GET https://connect.mindcloud.co/v1/universal/finaX/latest/actions/invoice-xml-from-zugferd
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a finaX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finaX/latest/actions/invoice-xml-from-zugferd?connectionId=$CONNECTION_ID&file=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "file": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finaX/latest/actions/invoice-xml-from-zugferd?${params}`, {
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
| `file` | file | yes | ZUGFeRD invoice file. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native finaX API returns.

## Native endpoint

Through the native finaX API, this operation is `POST /v1/pdf/xml/` (base URL `https://api.finax.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/invoice-xml-from-zugferd.md) for the provider-specific parameters and requirements.

