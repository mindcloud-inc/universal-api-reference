# Sendloop: Search Subscribers



```
GET https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/search-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendloop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/search-subscribers?connectionId=$CONNECTION_ID&emailAddress=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "emailAddress": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/search-subscribers?${params}`, {
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
| `emailAddress` | string | yes | Exact or partial email address to search for |

## Response

```json
{
  "success": true,
  "data": [
    {
      "listID": 1,
      "listName": "Ava Chen",
      "subscriberDetails": {
        "1": {
          "bounceType": "string",
          "customField2": "string",
          "subscriptionStatus": "string"
        }
      },
      "subscribers": {
        "1": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `listID` | number |  |
| `listName` | string |  |
| `subscriberDetails.1.bounceType` | string |  |
| `subscriberDetails.1.customField2` | string |  |
| `subscriberDetails.1.subscriptionStatus` | string |  |
| `subscribers.1` | string |  |

## Native endpoint

Through the native Sendloop API, this operation is `POST /subscriber.search/json` (base URL `https://{{credentials.subdomain}}.sendloop.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-subscribers.md) for the provider-specific parameters and requirements.

