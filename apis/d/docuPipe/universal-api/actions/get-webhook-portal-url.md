# DocuPipe: Get Webhook Portal URL

Retrieves the webhook portal URL from DocuPipe.

```
GET https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/get-webhook-portal-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPipe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/get-webhook-portal-url?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/get-webhook-portal-url?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `url` | string | Generates a magic link for you to log on to URL to the app portal. From the portal you can configure webhook subscriptions |

## Native endpoint

Through the native DocuPipe API, this operation is `GET /webhook/get-portal-link` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook-portal-url.md) for the provider-specific parameters and requirements.

