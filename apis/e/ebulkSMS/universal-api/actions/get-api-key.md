# EbulkSMS: Get API Key

Retrieves your EbulkSMS API key.

```
GET https://connect.mindcloud.co/v1/universal/ebulkSMS/latest/actions/get-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EbulkSMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ebulkSMS/latest/actions/get-api-key?connectionId=$CONNECTION_ID&auth.password=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "auth.password": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ebulkSMS/latest/actions/get-api-key?${params}`, {
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
| `auth.password` | string | yes | Your EbulkSMS account password. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": {
        "apikey": "string",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response.apikey` | string |  |
| `response.status` | string |  |

## Native endpoint

Through the native EbulkSMS API, this operation is `POST /getapikey.json` (base URL `https://api.ebulksms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-key.md) for the provider-specific parameters and requirements.

