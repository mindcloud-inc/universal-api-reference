# TouchBasePro: Get Lists For Email

Retrieves lists for an email address from TouchBasePro.

```
GET https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-lists-for-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TouchBasePro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-lists-for-email?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-lists-for-email?${params}`, {
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
      "dateSubscriberAdded": "2026-05-07T12:00:00.000Z",
      "listId": "string",
      "listName": "Ava Chen",
      "subscriberState": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateSubscriberAdded` | date |  |
| `listId` | string |  |
| `listName` | string |  |
| `subscriberState` | string |  |

## Native endpoint

Through the native TouchBasePro API, this operation is `GET /email/clients/listsforemail?email={email}` (base URL `https://api.touchbasepro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lists-for-email.md) for the provider-specific parameters and requirements.

