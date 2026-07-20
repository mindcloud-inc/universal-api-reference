# Merit: Get Sales Invoice PDF



```
GET https://connect.mindcloud.co/v1/universal/merit/latest/actions/get-sales-invoice-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Merit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/merit/latest/actions/get-sales-invoice-pdf?connectionId=$CONNECTION_ID&Id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "Id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/merit/latest/actions/get-sales-invoice-pdf?${params}`, {
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
| `Id` | string | yes | Sales invoice ID from Merit docs. |
| `DelivNote` | boolean | no | If true, generate delivery note without prices. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "FileContent": "string",
      "FileName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `FileContent` | string |  |
| `FileName` | string |  |

## Native endpoint

Through the native Merit API, this operation is `POST v2/getsalesinvpdf` (base URL `https://aktiva.merit.ee/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sales-invoice-pdf.md) for the provider-specific parameters and requirements.

