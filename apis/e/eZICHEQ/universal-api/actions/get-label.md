# EZICHEQ: Get Label

Retrieves a label from EZICHEQ.

```
GET https://connect.mindcloud.co/v1/universal/eZICHEQ/latest/actions/get-label
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EZICHEQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eZICHEQ/latest/actions/get-label?connectionId=$CONNECTION_ID&labelNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "labelNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eZICHEQ/latest/actions/get-label?${params}`, {
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
| `labelNumber` | string | yes |  |
| `labelNumber` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "date": "string",
      "error": "string",
      "request_method": "string",
      "request_uri": "string",
      "results": [
        {}
      ],
      "status": "string",
      "status_code": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `date` | string |  |
| `error` | string |  |
| `request_method` | string |  |
| `request_uri` | string |  |
| `results` | array<object> |  |
| `status` | string |  |
| `status_code` | number |  |

## Native endpoint

Through the native EZICHEQ API, this operation is `GET /label/v1/:labelNumber` (base URL `https://api.ezicheq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-label.md) for the provider-specific parameters and requirements.

