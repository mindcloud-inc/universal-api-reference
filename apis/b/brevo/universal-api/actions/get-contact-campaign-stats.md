# Brevo: Get Contact Campaign Stats



```
GET https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-contact-campaign-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brevo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-contact-campaign-stats?connectionId=$CONNECTION_ID&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-contact-campaign-stats?${params}`, {
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
| `identifier` | string | yes | The email address or contact id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clicked": 1,
      "messagesSent": 1,
      "opened": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clicked` | number | The number of clicks. |
| `messagesSent` | number | The number of messages sent to the contact. |
| `opened` | number | The number of opens. |

## Native endpoint

Through the native Brevo API, this operation is `GET /v3/contacts/:identifier/campaignStats` (base URL `https://api.brevo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-campaign-stats.md) for the provider-specific parameters and requirements.

