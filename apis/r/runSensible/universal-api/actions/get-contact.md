# RunSensible: Get Contact



```
GET https://connect.mindcloud.co/v1/universal/runSensible/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RunSensible `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runSensible/latest/actions/get-contact?connectionId=$CONNECTION_ID&id=c6aaa7ff-ff5e-45fe-bc53-973062b499c9" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "c6aaa7ff-ff5e-45fe-bc53-973062b499c9"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runSensible/latest/actions/get-contact?${params}`, {
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
| `id` | string | yes | The RunSensible contact id to retrieve. Example: `c6aaa7ff-ff5e-45fe-bc53-973062b499c9`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "communication": {
        "email": "ava@example.com"
      },
      "creationDate": "2026-05-07T12:00:00.000Z",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "owner": {
        "id": "string",
        "value": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `communication.email` | string |  |
| `creationDate` | date |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `owner.id` | string |  |
| `owner.value` | string |  |

## Native endpoint

Through the native RunSensible API, this operation is `GET /api/Person/Get` (base URL `https://app.runsensible.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

