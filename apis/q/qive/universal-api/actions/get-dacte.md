# Qive: Get DACTe



```
GET https://connect.mindcloud.co/v1/universal/qive/latest/actions/get-dacte
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qive/latest/actions/get-dacte?connectionId=$CONNECTION_ID&accessKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accessKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qive/latest/actions/get-dacte?${params}`, {
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
| `accessKey` | string | yes | CTe access key for the DACTe PDF. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access_key": "string",
      "encoded_pdf": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access_key` | string |  |
| `encoded_pdf` | string |  |

## Native endpoint

Through the native Qive API, this operation is `GET /v1/cte/dacte` (base URL `https://sandbox-api.arquivei.com.br`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dacte.md) for the provider-specific parameters and requirements.

