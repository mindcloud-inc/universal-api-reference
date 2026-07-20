# CoachAccountable: List Offerings

Retrieves offerings from CoachAccountable.

```
GET https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-offerings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-offerings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-offerings?${params}`, {
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
      "blurb": "string",
      "CoachID": 1,
      "description": "string",
      "ID": 1,
      "iframeURL": "https://example.com",
      "name": "Ava Chen",
      "notifyEmail": "ava@example.com",
      "price": 1,
      "scriptURL": "https://example.com",
      "URL": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blurb` | string |  |
| `CoachID` | number |  |
| `description` | string |  |
| `ID` | number |  |
| `iframeURL` | string |  |
| `name` | string |  |
| `notifyEmail` | string |  |
| `price` | number |  |
| `scriptURL` | string |  |
| `URL` | string |  |

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-offerings.md) for the provider-specific parameters and requirements.

