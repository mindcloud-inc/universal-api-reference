# SigningHub: Get Package Details

Retrieves package details from SigningHub.

```
GET https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/get-package-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigningHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/get-package-details?connectionId=$CONNECTION_ID&packageId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "packageId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/get-package-details?${params}`, {
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
| `packageId` | number | yes | Package ID of the document package. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "document_status": "string",
      "documents": [
        {}
      ],
      "name": "Ava Chen",
      "owner": {},
      "read_only": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `document_status` | string |  |
| `documents` | array<object> |  |
| `name` | string |  |
| `owner` | object |  |
| `read_only` | boolean |  |

## Native endpoint

Through the native SigningHub API, this operation is `GET /v4/packages/:packageId/details` (base URL `https://api.signinghub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-package-details.md) for the provider-specific parameters and requirements.

