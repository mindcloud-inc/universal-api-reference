# Certs 365: Get Single Certificates

Retrieves single certificates from Certs 365 storage.

```
GET https://connect.mindcloud.co/v1/universal/certs365/latest/actions/get-single-certificates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Certs 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/certs365/latest/actions/get-single-certificates?connectionId=$CONNECTION_ID&issuerId=string&type=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "issuerId": "string",
  "type": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/certs365/latest/actions/get-single-certificates?${params}`, {
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
| `issuerId` | string | yes | Issuer ID. |
| `type` | number | yes | Certificate type: 1 with PDF, 2 without PDF. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Certs 365 API, this operation is `POST /api/get-single-certificates` (base URL `https://api1.certs365.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-single-certificates.md) for the provider-specific parameters and requirements.

