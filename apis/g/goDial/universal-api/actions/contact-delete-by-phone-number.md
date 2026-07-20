# GoDial: Delete Contact by Phone Number

Deletes a contact from GoDial by phone number and list ID.

```
DELETE https://connect.mindcloud.co/v1/universal/goDial/latest/actions/contact-delete-by-phone-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoDial `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/goDial/latest/actions/contact-delete-by-phone-number?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goDial/latest/actions/contact-delete-by-phone-number?${params}`, {
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
      "count": 1,
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `message` | string |  |

## Native endpoint

Through the native GoDial API, this operation is `POST /externals/contact/delete-by-phone` (base URL `https://enterprise.godial.cc/meta/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/contact-delete-by-phone-number.md) for the provider-specific parameters and requirements.

