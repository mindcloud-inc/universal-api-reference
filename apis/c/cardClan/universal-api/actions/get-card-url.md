# CardClan: Get Card URL

Generates a personalized CardClan card URL without sending email.

```
GET https://connect.mindcloud.co/v1/universal/cardClan/latest/actions/get-card-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CardClan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cardClan/latest/actions/get-card-url?connectionId=$CONNECTION_ID&card=string&integrationId=string&mergeTags%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "card": "string",
  "integrationId": "string",
  "mergeTags[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cardClan/latest/actions/get-card-url?${params}`, {
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
| `card` | string | yes | Card ID for URL generation. |
| `integrationId` | string | yes | Integration configuration ID. |
| `mergeTags[]` | array<object> | yes | Array of merge tag objects with recipient data. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "card_cover": "string",
      "unsubscribe_link_url": "https://example.com",
      "view_card_url": "https://example.com",
      "white_label_app_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `card_cover` | string | Card cover image URL. |
| `unsubscribe_link_url` | string | Recipient unsubscribe link URL. |
| `view_card_url` | string | Generated card view URL. |
| `white_label_app_name` | string | White-label app name associated with the generated URL. |

## Native endpoint

Through the native CardClan API, this operation is `POST /integration/get-card-url` (base URL `https://app.cardclan.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-card-url.md) for the provider-specific parameters and requirements.

