# ECAL: Get Subscriber By Email

Retrieves an ECAL subscriber by email address.

```
GET https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/get-subscriber-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ECAL `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/get-subscriber-by-email?connectionId=$CONNECTION_ID&emailAddress=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "emailAddress": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/get-subscriber-by-email?${params}`, {
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
| `emailAddress` | string | yes | Subscriber email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "calendarIds": [
        "string"
      ],
      "ecalId": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "lastName": "Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calendarIds` | array<string> |  |
| `ecalId` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `status` | string |  |

## Native endpoint

Through the native ECAL API, this operation is `GET /subscriber/:emailAddress` (base URL `https://api.ecal.com/apiv2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscriber-by-email.md) for the provider-specific parameters and requirements.

