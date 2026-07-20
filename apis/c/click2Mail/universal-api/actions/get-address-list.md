# Click2Mail: Get Address List

Retrieves an address list from Click2Mail.

```
GET https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/get-address-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Click2Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/get-address-list?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/get-address-list?${params}`, {
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
| `id` | number | yes | base address list id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addressListsInfo": [
        {}
      ],
      "count": 1,
      "description": "string",
      "id": 1,
      "status": 1,
      "statusLocation": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addressListsInfo` | array<object> |  |
| `count` | number |  |
| `description` | string |  |
| `id` | number |  |
| `status` | number |  |
| `statusLocation` | string |  |

## Native endpoint

Through the native Click2Mail API, this operation is `GET /molpro/addressLists/{id}` (base URL `https://stage-rest.click2mail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-address-list.md) for the provider-specific parameters and requirements.

