# Routee: Retrieve the account's contact labels

Retrieves the account's contact labels from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-the-accounts-contact-labels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-the-accounts-contact-labels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-the-accounts-contact-labels?${params}`, {
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
      "age": "string",
      "country": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "lastName": "Chen",
      "mobile": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `age` | string |  |
| `country` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `mobile` | string |  |

## Native endpoint

Through the native Routee API, this operation is `GET /contacts/labels/my` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-the-accounts-contact-labels.md) for the provider-specific parameters and requirements.

