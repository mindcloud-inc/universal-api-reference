# lemlist: Get Team Credits

Retrieves your team credits from lemlist.

```
GET https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/get-team-credits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a lemlist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/get-team-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/get-team-credits?${params}`, {
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
      "credits": 1,
      "details": {
        "remaining": {
          "freemium": 1,
          "gifted": 1,
          "paid": 1,
          "subscription": 1,
          "total": 1
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits` | number | Remaining team credits. |
| `details.remaining.freemium` | number | Remaining freemium credits. |
| `details.remaining.gifted` | number | Remaining gifted credits. |
| `details.remaining.paid` | number | Remaining paid credits. |
| `details.remaining.subscription` | number | Remaining subscription credits. |
| `details.remaining.total` | number | Total remaining credits. |

## Native endpoint

Through the native lemlist API, this operation is `GET /team/credits` (base URL `https://api.lemlist.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team-credits.md) for the provider-specific parameters and requirements.

