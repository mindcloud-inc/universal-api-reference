# Envoice: Get Client Details

Retrieves client details from Envoice.

```
GET https://connect.mindcloud.co/v1/universal/envoice/latest/actions/get-client-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Envoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/envoice/latest/actions/get-client-details?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/envoice/latest/actions/get-client-details?${params}`, {
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
| `id` | number | yes | Client identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Activities": [
        {}
      ],
      "Email": "ava@example.com",
      "Id": 1,
      "Invoices": [
        {}
      ],
      "Name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Activities` | array<object> | Client activities. |
| `Email` | string | Client email. |
| `Id` | number | Client identifier. |
| `Invoices` | array<object> | Client invoices. |
| `Name` | string | Client name. |

## Native endpoint

Through the native Envoice API, this operation is `GET client/details` (base URL `https://www.envoice.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client-details.md) for the provider-specific parameters and requirements.

