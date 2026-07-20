# mittwald: Get Mail Address

Retrieves mail address from mittwald API.

```
GET https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/get-mail-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a mittwald `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/get-mail-address?connectionId=$CONNECTION_ID&mailAddressId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mailAddressId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/get-mail-address?${params}`, {
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
| `mailAddressId` | string | yes | The unique identifier of the mail address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "forwardAddresses": [
        "string"
      ],
      "id": "string",
      "projectId": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `forwardAddresses` | array<string> |  |
| `id` | string |  |
| `projectId` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native mittwald API, this operation is `GET /v2/mail-addresses/:mailAddressId` (base URL `https://api.mittwald.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-mail-address.md) for the provider-specific parameters and requirements.

