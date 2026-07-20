# Minelead: List Recipient Lists

Retrieves recipient lists from your Minelead account.

```
GET https://connect.mindcloud.co/v1/universal/minelead/latest/actions/list-recipient-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Minelead `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/minelead/latest/actions/list-recipient-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/minelead/latest/actions/list-recipient-lists?${params}`, {
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
      "recipient_list": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `recipient_list` | array<object> |  |
| `status` | string |  |

## Native endpoint

Through the native Minelead API, this operation is `GET /campaigns-recipients` (base URL `https://api.minelead.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-recipient-lists.md) for the provider-specific parameters and requirements.

