# CreateSend: Get Subscriber Details

Retrieves subscriber details from CreateSend by email address.

```
GET https://connect.mindcloud.co/v1/universal/createSend/latest/actions/get-subscriber-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CreateSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/createSend/latest/actions/get-subscriber-details?connectionId=$CONNECTION_ID&listId=string&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "string",
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/createSend/latest/actions/get-subscriber-details?${params}`, {
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
| `listId` | string | yes |  |
| `email` | string | yes |  |
| `includeTrackingPreference` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "EmailAddress": "ava@example.com",
      "Name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `EmailAddress` | string | Subscriber email address. |
| `Name` | string | Subscriber name. |

## Native endpoint

Through the native CreateSend API, this operation is `GET /subscribers/:listId.json` (base URL `https://api.createsend.com/api/v3.3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscriber-details.md) for the provider-specific parameters and requirements.

