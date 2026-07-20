# DirectIQ: List Date Keys

Retrieves date-type contact keys from DirectIQ.

```
GET https://connect.mindcloud.co/v1/universal/directiq/latest/actions/list-date-keys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DirectIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/directiq/latest/actions/list-date-keys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/directiq/latest/actions/list-date-keys?${params}`, {
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
      "id": 1,
      "keyName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `keyName` | string |  |

## Native endpoint

Through the native DirectIQ API, this operation is `GET /contacts/extradata/listdatekeys` (base URL `https://rest.directiq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-date-keys.md) for the provider-specific parameters and requirements.

