# Mallabe: Get Website Status

Retrieves website status details from Mallabe.

```
GET https://connect.mindcloud.co/v1/universal/mallabe/latest/actions/get-website-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mallabe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mallabe/latest/actions/get-website-status?connectionId=$CONNECTION_ID&website=string&method=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "website": "string",
  "method": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mallabe/latest/actions/get-website-status?${params}`, {
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
| `website` | string | yes | Website URL to check. |
| `method` | string | yes | HTTP method to use for the website check. |
| `webhookUrl` | string | no | Webhook URL for asynchronous callbacks. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alive": true,
      "checkDate": "2026-05-07T12:00:00.000Z",
      "timeTook": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alive` | boolean |  |
| `checkDate` | date |  |
| `timeTook` | number |  |

## Native endpoint

Through the native Mallabe API, this operation is `POST /websites/status` (base URL `https://mallabe.p.rapidapi.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-website-status.md) for the provider-specific parameters and requirements.

