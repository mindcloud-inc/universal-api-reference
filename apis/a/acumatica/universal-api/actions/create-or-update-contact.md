# Acumatica: Create or Update Contact



```
PUT https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/create-or-update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/create-or-update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "LastName.value": "Test Contact"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/create-or-update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "LastName.value": "Test Contact"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `FirstName` | object | no |  |
| `FirstName.value` | string | no | Example: `Jamie`. |
| `LastName` | object | no |  |
| `LastName.value` | string | yes | Example: `Test Contact`. |
| `Email` | object | no |  |
| `Email.value` | string | no | Example: `test@example.com`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ContactID` | object | no |  |
| `ContactID.value` | number | no | Existing numeric Contact ID when updating; leave blank to create. |
| `BusinessAccount` | object | no |  |
| `BusinessAccount.value` | string | no |  |
| `Type` | object | no |  |
| `Type.value` | string | no |  |

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
      "LastModifiedDateTime": {
        "value": "2026-05-07T12:00:00.000Z"
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
      "NoteID": {
        "value": "string"
      },
      "OverrideAccountAddress": {
        "value": true
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
      "Status": {
        "value": "string"
      },
      "Synchronize": {
        "value": true
      },
      "Type": {
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
| `LastModifiedDateTime.value` | date |  |
| `LastName.value` | string |  |
| `NoMarketing.value` | boolean |  |
| `NoMassMail.value` | boolean |  |
| `NoteID.value` | string |  |
| `OverrideAccountAddress.value` | boolean |  |
| `Phone1Type.value` | string |  |
| `Phone2Type.value` | string |  |
| `Phone3Type.value` | string |  |
| `rowNumber` | number |  |
| `Status.value` | string |  |
| `Synchronize.value` | boolean |  |
| `Type.value` | string |  |

## Native endpoint

Through the native Acumatica API, this operation is `PUT /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Contact` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-contact.md) for the provider-specific parameters and requirements.

