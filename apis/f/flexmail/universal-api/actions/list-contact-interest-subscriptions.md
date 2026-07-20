# Flexmail: List Contact Interest Subscriptions

Retrieves interest subscriptions for a contact from Flexmail.

```
GET https://connect.mindcloud.co/v1/universal/flexmail/latest/actions/list-contact-interest-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flexmail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flexmail/latest/actions/list-contact-interest-subscriptions?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flexmail/latest/actions/list-contact-interest-subscriptions?${params}`, {
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
| `id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_embedded": {},
      "interest_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_embedded` | object | Embedded interest details when provided by Flexmail. |
| `interest_id` | string | The identifier of the subscribed interest. |

## Native endpoint

Through the native Flexmail API, this operation is `GET /contacts/{id}/interest-subscriptions` (base URL `https://api.flexmail.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-interest-subscriptions.md) for the provider-specific parameters and requirements.

