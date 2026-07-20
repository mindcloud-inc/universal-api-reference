# Docage: Get Docage User By ID

Retrieves a user from Docage by ID.

```
GET https://connect.mindcloud.co/v1/universal/docage/latest/actions/get-docage-user-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docage/latest/actions/get-docage-user-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docage/latest/actions/get-docage-user-by-id?${params}`, {
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
| `id` | string | yes | The Docage user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AlertEnabled": true,
      "ApplicationUserId": "string",
      "Company": "string",
      "CourrierEnabled": true,
      "EbpUserName": "Ava Chen",
      "Email": "ava@example.com",
      "FirstName": "Ava",
      "GdprEnabled": true,
      "Gender": 1,
      "Job": "string",
      "Language": 1,
      "LastName": "Chen",
      "SignatureEnabled": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AlertEnabled` | boolean |  |
| `ApplicationUserId` | string |  |
| `Company` | string |  |
| `CourrierEnabled` | boolean |  |
| `EbpUserName` | string |  |
| `Email` | string |  |
| `FirstName` | string |  |
| `GdprEnabled` | boolean |  |
| `Gender` | number |  |
| `Job` | string |  |
| `Language` | number |  |
| `LastName` | string |  |
| `SignatureEnabled` | boolean |  |

## Native endpoint

Through the native Docage API, this operation is `GET /DocageUsers/ById/:id` (base URL `https://api.docage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-docage-user-by-id.md) for the provider-specific parameters and requirements.

