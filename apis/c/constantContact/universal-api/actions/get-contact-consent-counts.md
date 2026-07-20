# Constant Contact: Get Contact Consent Counts

Retrieves contact consent counts from Constant Contact.

```
GET https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/get-contact-consent-counts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Constant Contact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/get-contact-consent-counts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/get-contact-consent-counts?${params}`, {
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
| `include` | string | no | Include optional count detail (for example `new_subscriber`). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "explicit": 1,
      "implicit": 1,
      "pending": 1,
      "total": 1,
      "unsubscribed": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `explicit` | number |  |
| `implicit` | number |  |
| `pending` | number |  |
| `total` | number |  |
| `unsubscribed` | number |  |

## Native endpoint

Through the native Constant Contact API, this operation is `GET /contacts/counts` (base URL `https://api.cc.email/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-consent-counts.md) for the provider-specific parameters and requirements.

