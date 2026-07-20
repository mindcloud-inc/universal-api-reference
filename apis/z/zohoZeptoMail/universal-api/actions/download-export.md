# Zoho ZeptoMail: Download Export

Downloads a log export from Zoho ZeptoMail.

```
GET https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/download-export
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho ZeptoMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/download-export?connectionId=$CONNECTION_ID&exportType=string&exportId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "exportType": "string",
  "exportId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/download-export?${params}`, {
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
| `exportType` | string | yes | Export category to download from. |
| `exportId` | string | yes | Export job identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string |  |

## Native endpoint

Through the native Zoho ZeptoMail API, this operation is `GET :exportType/exports/:exportId/download` (base URL `https://api.zeptomail.com/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-export.md) for the provider-specific parameters and requirements.

