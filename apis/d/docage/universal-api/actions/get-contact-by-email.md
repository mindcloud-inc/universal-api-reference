# Docage: Get Contact By Email

Retrieves a contact from Docage by email.

```
GET https://connect.mindcloud.co/v1/universal/docage/latest/actions/get-contact-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docage/latest/actions/get-contact-by-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docage/latest/actions/get-contact-by-email?${params}`, {
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
| `email` | string | yes | The Docage contact email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "BoxContacts": [
        "string"
      ],
      "Boxes": [
        "string"
      ],
      "Civility": "string",
      "Company": "string",
      "Country": "string",
      "Email": "ava@example.com",
      "FirstName": "Ava",
      "Gender": 1,
      "Job": "string",
      "Language": 1,
      "LastName": "Chen",
      "Mobile": "string",
      "Phone": "string",
      "TransactionMembers": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `BoxContacts` | array |  |
| `Boxes` | array |  |
| `Civility` | string |  |
| `Company` | string |  |
| `Country` | string |  |
| `Email` | string |  |
| `FirstName` | string |  |
| `Gender` | number |  |
| `Job` | string |  |
| `Language` | number |  |
| `LastName` | string |  |
| `Mobile` | string |  |
| `Phone` | string |  |
| `TransactionMembers` | array |  |

## Native endpoint

Through the native Docage API, this operation is `GET /Contacts/byemail/:email` (base URL `https://api.docage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-by-email.md) for the provider-specific parameters and requirements.

