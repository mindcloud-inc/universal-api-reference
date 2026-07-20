# Zoho Sign: Get Document Form Data

Retrieves document form data from Zoho Sign.

```
GET https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/get-document-form-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/get-document-form-data?connectionId=$CONNECTION_ID&requestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/get-document-form-data?${params}`, {
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
| `requestId` | string | yes | Zoho Sign request identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "documentFormData": {
        "requestName": "Ava Chen",
        "zsDocumentId": "string"
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `documentFormData` | object |  |
| `documentFormData.requestName` | string |  |
| `documentFormData.zsDocumentId` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho Sign API, this operation is `GET /requests/:requestId/fielddata` (base URL `https://sign.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document-form-data.md) for the provider-specific parameters and requirements.

