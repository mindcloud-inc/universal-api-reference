# Routee: Retrieve total amount of sent emails

Retrieves total amount of sent emails from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-total-amount-of-sent-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-total-amount-of-sent-emails?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-total-amount-of-sent-emails?${params}`, {
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
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `total` | number |  |

## Native endpoint

Through the native Routee API, this operation is `GET /smtp/emails/total` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-total-amount-of-sent-emails.md) for the provider-specific parameters and requirements.

