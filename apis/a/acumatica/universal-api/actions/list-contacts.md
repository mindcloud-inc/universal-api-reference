# Acumatica: List Contacts



```
GET https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/list-contacts?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `select` | string | no | Comma-separated entity fields to return. Example: `ContactID,DisplayName,Email,Status`. |
| `expand` | string | no | Comma-separated detail or linked entities to expand. Example: `Address,Attributes`. |
| `filter` | string | no | Acumatica OData filter expression used to qualify returned records. Example: `Status eq 'Active'`. |
| `custom` | string | no | Comma-separated custom fields to return. Example: `DisplayName,Email`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {
        "files:put": "https://example.com",
        "self": "https://example.com"
      },
      "Active": {
        "value": true
      },
      "CompanyName": {
        "value": "Ava Chen"
      },
      "ContactClass": {
        "value": "string"
      },
      "ContactID": {
        "value": 1
      },
      "ContactMethod": {
        "value": "string"
      },
      "DisplayName": {
        "value": "Ava Chen"
      },
      "DoNotCall": {
        "value": true
      },
      "DoNotEmail": {
        "value": true
      },
      "DoNotFax": {
        "value": true
      },
      "DoNotMail": {
        "value": true
      },
      "Duplicate": {
        "value": "string"
      },
      "DuplicateFound": {
        "value": true
      },
      "Email": {
        "value": "ava@example.com"
      },
      "FaxType": {
        "value": "string"
      },
      "FirstName": {
        "value": "Ava"
      },
      "id": "string",
      "JobTitle": {
        "value": "string"
      },
      "LastModifiedDateTime": {
        "value": "string"
      },
      "LastName": {
        "value": "Chen"
      },
      "NoMarketing": {
        "value": true
      },
      "NoMassMail": {
        "value": true
      },
      "note": {
        "value": "string"
      },
      "NoteID": {
        "value": "string"
      },
      "Owner": {
        "value": "string"
      },
      "OwnerEmployeeName": {
        "value": "Ava Chen"
      },
      "Phone1": {
        "value": "string"
      },
      "Phone1Type": {
        "value": "string"
      },
      "Phone2Type": {
        "value": "string"
      },
      "Phone3Type": {
        "value": "string"
      },
      "rowNumber": 1,
      "Source": {
        "value": "string"
      },
      "Status": {
        "value": "string"
      },
      "Type": {
        "value": "string"
      },
      "Workgroup": {
        "value": "string"
      },
      "WorkgroupDescription": {
        "value": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links.files:put` | string |  |
| `_links.self` | string |  |
| `Active.value` | boolean |  |
| `CompanyName.value` | string |  |
| `ContactClass.value` | string |  |
| `ContactID.value` | number |  |
| `ContactMethod.value` | string |  |
| `DisplayName.value` | string |  |
| `DoNotCall.value` | boolean |  |
| `DoNotEmail.value` | boolean |  |
| `DoNotFax.value` | boolean |  |
| `DoNotMail.value` | boolean |  |
| `Duplicate.value` | string |  |
| `DuplicateFound.value` | boolean |  |
| `Email.value` | string |  |
| `FaxType.value` | string |  |
| `FirstName.value` | string |  |
| `id` | string |  |
| `JobTitle.value` | string |  |
| `LastModifiedDateTime.value` | string |  |
| `LastName.value` | string |  |
| `NoMarketing.value` | boolean |  |
| `NoMassMail.value` | boolean |  |
| `note.value` | string |  |
| `NoteID.value` | string |  |
| `Owner.value` | string |  |
| `OwnerEmployeeName.value` | string |  |
| `Phone1.value` | string |  |
| `Phone1Type.value` | string |  |
| `Phone2Type.value` | string |  |
| `Phone3Type.value` | string |  |
| `rowNumber` | number |  |
| `Source.value` | string |  |
| `Status.value` | string |  |
| `Type.value` | string |  |
| `Workgroup.value` | string |  |
| `WorkgroupDescription.value` | string |  |

## Native endpoint

Through the native Acumatica API, this operation is `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Contact` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

