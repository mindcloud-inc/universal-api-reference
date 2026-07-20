# DirectIQ: List Client Contact Keys

Retrieves client contact keys from DirectIQ.

```
GET https://connect.mindcloud.co/v1/universal/directiq/latest/actions/list-client-contact-keys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DirectIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/directiq/latest/actions/list-client-contact-keys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/directiq/latest/actions/list-client-contact-keys?${params}`, {
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
      "clientKeys": [
        [
          {}
        ]
      ],
      "emailCount": 1,
      "firstNameCount": 1,
      "lastNameCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientKeys[]` | array<object> |  |
| `clientKeys[].dateFormat` | string |  |
| `clientKeys[].id` | number |  |
| `clientKeys[].isPublic` | boolean |  |
| `clientKeys[].name` | string |  |
| `clientKeys[].shortCode` | string |  |
| `clientKeys[].totalCount` | number |  |
| `clientKeys[].valueType` | number |  |
| `emailCount` | number |  |
| `firstNameCount` | number |  |
| `lastNameCount` | number |  |

## Native endpoint

Through the native DirectIQ API, this operation is `GET /contacts/extradata/list` (base URL `https://rest.directiq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-client-contact-keys.md) for the provider-specific parameters and requirements.

