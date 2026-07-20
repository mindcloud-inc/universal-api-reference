# Click2Mail: Check Address List Name

Checks whether an address list name is available in Click2Mail.

```
GET https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/check-address-list-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Click2Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/check-address-list-name?connectionId=$CONNECTION_ID&addressListName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "addressListName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/check-address-list-name?${params}`, {
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
| `addressListName` | string | yes | Address List name as it will be stored in your account |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native Click2Mail API, this operation is `POST /molpro/addressLists/checkName` (base URL `https://stage-rest.click2mail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-address-list-name.md) for the provider-specific parameters and requirements.

