# Kiwili: Get Contact Details

Retrieves details for a contact in Kiwili.

```
GET https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-contact-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kiwili `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-contact-details?connectionId=$CONNECTION_ID&contact_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contact_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-contact-details?${params}`, {
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
| `contact_id` | number | yes | The Kiwili contact ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Email": "ava@example.com",
      "EnterpriseId": 1,
      "FirstName": "Ava",
      "Id": 1,
      "IsActive": true,
      "LastName": "Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Email` | string |  |
| `EnterpriseId` | number |  |
| `FirstName` | string |  |
| `Id` | number |  |
| `IsActive` | boolean |  |
| `LastName` | string |  |

## Native endpoint

Through the native Kiwili API, this operation is `GET /contact/:contact_id` (base URL `https://mindcloud.kiwili.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-details.md) for the provider-specific parameters and requirements.

