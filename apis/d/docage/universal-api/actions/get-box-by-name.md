# Docage: Get Box By Name

Retrieves a box from Docage by name.

```
GET https://connect.mindcloud.co/v1/universal/docage/latest/actions/get-box-by-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docage/latest/actions/get-box-by-name?connectionId=$CONNECTION_ID&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docage/latest/actions/get-box-by-name?${params}`, {
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
| `name` | string | yes | The Docage box name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ArchiveEndDate": "string",
      "ArchiveStartDate": "string",
      "BoxFiles": [
        "string"
      ],
      "ContactsNb": 1,
      "CreatorId": "string",
      "CreatorName": "Ava Chen",
      "Description": "string",
      "DocageUsersNb": 1,
      "DocumentsNb": 1,
      "EntityState": 1,
      "Name": "Ava Chen",
      "Notes": "string",
      "ParentOrganizationId": "string",
      "TransactionsNb": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ArchiveEndDate` | string |  |
| `ArchiveStartDate` | string |  |
| `BoxFiles` | array |  |
| `ContactsNb` | number |  |
| `CreatorId` | string |  |
| `CreatorName` | string |  |
| `Description` | string |  |
| `DocageUsersNb` | number |  |
| `DocumentsNb` | number |  |
| `EntityState` | number |  |
| `Name` | string |  |
| `Notes` | string |  |
| `ParentOrganizationId` | string |  |
| `TransactionsNb` | number |  |

## Native endpoint

Through the native Docage API, this operation is `GET /Boxes/ByName/:name` (base URL `https://api.docage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-box-by-name.md) for the provider-specific parameters and requirements.

