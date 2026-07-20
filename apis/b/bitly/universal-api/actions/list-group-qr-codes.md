# Bitly: List Group QR Codes

Retrieves QR codes for a group in Bitly.

```
GET https://connect.mindcloud.co/v1/universal/bitly/latest/actions/list-group-qr-codes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bitly/latest/actions/list-group-qr-codes?connectionId=$CONNECTION_ID&groupGuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupGuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bitly/latest/actions/list-group-qr-codes?${params}`, {
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
| `groupGuid` | string | yes |  |
| `size` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {
        "next": "string",
        "searchAfter": "string",
        "size": 1
      },
      "qrCodes": [
        {
          "archived": true,
          "created": "string",
          "groupGuid": "string",
          "longUrls": [
            "https://example.com"
          ],
          "qrcodeId": "string",
          "qrCodeType": "string",
          "title": "string",
          "updated": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination.next` | string |  |
| `pagination.searchAfter` | string |  |
| `pagination.size` | number |  |
| `qrCodes[].archived` | boolean |  |
| `qrCodes[].created` | string |  |
| `qrCodes[].groupGuid` | string |  |
| `qrCodes[].longUrls[]` | string |  |
| `qrCodes[].qrcodeId` | string |  |
| `qrCodes[].qrCodeType` | string |  |
| `qrCodes[].title` | string |  |
| `qrCodes[].updated` | string |  |

## Native endpoint

Through the native Bitly API, this operation is `GET /groups/:group_guid/qr-codes` (base URL `https://api-ssl.bitly.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-group-qr-codes.md) for the provider-specific parameters and requirements.

