# Sendloop: Get Subscriber



```
GET https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/get-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendloop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/get-subscriber?connectionId=$CONNECTION_ID&listId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/get-subscriber?${params}`, {
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
| `listId` | number | yes | ID of the target list to get the subscriber from |
| `subscriberId` | number | no | ID number of the target subscriber |
| `emailAddress` | string | no | Email address of the subscriber |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bounceType": "string",
      "emailAddress": "ava@example.com",
      "optInDate": "2026-05-07T12:00:00.000Z",
      "subscriberID": 1,
      "subscriptionDate": "2026-05-07T12:00:00.000Z",
      "subscriptionIP": "string",
      "subscriptionStatus": "string",
      "unsubscriptionDate": "2026-05-07T12:00:00.000Z",
      "unsubscriptionIP": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bounceType` | string |  |
| `emailAddress` | string |  |
| `optInDate` | date |  |
| `subscriberID` | number |  |
| `subscriptionDate` | date |  |
| `subscriptionIP` | string |  |
| `subscriptionStatus` | string |  |
| `unsubscriptionDate` | date |  |
| `unsubscriptionIP` | string |  |

## Native endpoint

Through the native Sendloop API, this operation is `POST /subscriber.get/json` (base URL `https://{{credentials.subdomain}}.sendloop.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscriber.md) for the provider-specific parameters and requirements.

