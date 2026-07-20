# RegFox: List Forms

Retrieves forms from the RegFox account.

```
GET https://connect.mindcloud.co/v1/universal/regFox/latest/actions/list-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RegFox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/regFox/latest/actions/list-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/regFox/latest/actions/list-forms?${params}`, {
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
      "data": [
        {}
      ],
      "hasMore": true,
      "responseCode": 1,
      "startingAfter": 1,
      "totalResults": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Forms returned for the authenticated RegFox account. |
| `hasMore` | boolean | Whether more form records are available. |
| `responseCode` | number | HTTP-style response code returned by Webconnex. |
| `startingAfter` | number | Pagination cursor returned by the API. |
| `totalResults` | number | Total number of matching forms. |

## Native endpoint

Through the native RegFox API, this operation is `GET forms` (base URL `https://api.webconnex.com/v2/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-forms.md) for the provider-specific parameters and requirements.

