# Reverse Contact: Fetch Company Profile Live



```
GET https://connect.mindcloud.co/v1/universal/reverseContact/latest/actions/fetch-company-profile-live
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reverse Contact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reverseContact/latest/actions/fetch-company-profile-live?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reverseContact/latest/actions/fetch-company-profile-live?${params}`, {
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
| `url` | string | yes | Public Social company URL to fetch live. |
| `webhookUrl` | string | no | HTTPS callback URL for live results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string",
      "webhookId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |
| `webhookId` | string |  |

## Native endpoint

Through the native Reverse Contact API, this operation is `POST /v2/fetch/companies/live` (base URL `https://api.reversecontact.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-company-profile-live.md) for the provider-specific parameters and requirements.

