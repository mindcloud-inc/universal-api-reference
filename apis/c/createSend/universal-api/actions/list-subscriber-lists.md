# CreateSend: List Subscriber Lists

Retrieves subscriber lists for a client in CreateSend.

```
GET https://connect.mindcloud.co/v1/universal/createSend/latest/actions/list-subscriber-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CreateSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/createSend/latest/actions/list-subscriber-lists?connectionId=$CONNECTION_ID&clientId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clientId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/createSend/latest/actions/list-subscriber-lists?${params}`, {
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
| `clientId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ListID": "string",
      "Name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ListID` | string |  |
| `Name` | string |  |

## Native endpoint

Through the native CreateSend API, this operation is `GET /clients/:clientId/lists.json` (base URL `https://api.createsend.com/api/v3.3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subscriber-lists.md) for the provider-specific parameters and requirements.

