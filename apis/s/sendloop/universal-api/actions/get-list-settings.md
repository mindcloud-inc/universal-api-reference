# Sendloop: Get List Settings



```
GET https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/get-list-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendloop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/get-list-settings?connectionId=$CONNECTION_ID&listId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/get-list-settings?${params}`, {
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
| `listId` | number | yes | ID number of the target subscriber list |

## Response

```json
{
  "success": true,
  "data": [
    {
      "subscriptionFinalAction": "string",
      "subscriptionFinalFromEmail": "ava@example.com",
      "subscriptionFinalFromName": "Ava Chen",
      "subscriptionFinalHTMLBody": "string",
      "subscriptionFinalPlainBody": "string",
      "subscriptionFinalSubject": "string",
      "subscriptionOptInFromEmail": "ava@example.com",
      "subscriptionOptInFromName": "Ava Chen",
      "subscriptionOptInPlainBody": "string",
      "subscriptionOptInSubject": "string",
      "webServiceSubscriptionURL": "https://example.com",
      "webServiceUnsubscriptionURL": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `subscriptionFinalAction` | string |  |
| `subscriptionFinalFromEmail` | string |  |
| `subscriptionFinalFromName` | string |  |
| `subscriptionFinalHTMLBody` | string |  |
| `subscriptionFinalPlainBody` | string |  |
| `subscriptionFinalSubject` | string |  |
| `subscriptionOptInFromEmail` | string |  |
| `subscriptionOptInFromName` | string |  |
| `subscriptionOptInPlainBody` | string |  |
| `subscriptionOptInSubject` | string |  |
| `webServiceSubscriptionURL` | string |  |
| `webServiceUnsubscriptionURL` | string |  |

## Native endpoint

Through the native Sendloop API, this operation is `POST /list.settings.get/json` (base URL `https://{{credentials.subdomain}}.sendloop.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list-settings.md) for the provider-specific parameters and requirements.

