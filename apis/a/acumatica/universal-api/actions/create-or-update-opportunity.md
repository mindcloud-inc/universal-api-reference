# Acumatica: Create or Update Opportunity



```
PUT https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/create-or-update-opportunity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/create-or-update-opportunity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "Subject.value": "MindCloud test opportunity"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/create-or-update-opportunity', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "Subject.value": "MindCloud test opportunity"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `Subject` | object | no |  |
| `Subject.value` | string | yes | Example: `MindCloud test opportunity`. |
| `ClassID` | object | no |  |
| `ClassID.value` | string | no |  |
| `BusinessAccount` | object | no |  |
| `BusinessAccount.value` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `OpportunityID` | object | no |  |
| `OpportunityID.value` | string | no | Existing Opportunity ID when updating; leave blank to create. |
| `ContactID` | object | no |  |
| `ContactID.value` | number | no |  |
| `Stage` | object | no |  |
| `Stage.value` | string | no |  |

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
      "Amount": {
        "value": 1
      },
      "Branch": {
        "value": "string"
      },
      "BusinessAccount": {
        "value": "string"
      },
      "ClassID": {
        "value": "string"
      },
      "ContactDisplayName": {
        "value": "Ava Chen"
      },
      "ContactID": {
        "value": 1
      },
      "CurrencyID": {
        "value": "string"
      },
      "CurrencyViewState": {
        "value": true
      },
      "Discount": {
        "value": 1
      },
      "Estimation": {
        "value": "2026-05-07T12:00:00.000Z"
      },
      "id": "string",
      "LastModifiedDateTime": {
        "value": "2026-05-07T12:00:00.000Z"
      },
      "Location": {
        "value": "string"
      },
      "ManualAmount": {
        "value": true
      },
      "NoteID": {
        "value": "string"
      },
      "OpportunityID": {
        "value": "string"
      },
      "Override": {
        "value": true
      },
      "Project": {
        "value": "string"
      },
      "Reason": {
        "value": "string"
      },
      "rowNumber": 1,
      "Source": {
        "value": "string"
      },
      "Stage": {
        "value": "string"
      },
      "Status": {
        "value": "string"
      },
      "Subject": {
        "value": "string"
      },
      "Total": {
        "value": 1
      },
      "WeightTotal": {
        "value": 1
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
| `Amount.value` | number |  |
| `Branch.value` | string |  |
| `BusinessAccount.value` | string |  |
| `ClassID.value` | string |  |
| `ContactDisplayName.value` | string |  |
| `ContactID.value` | number |  |
| `CurrencyID.value` | string |  |
| `CurrencyViewState.value` | boolean |  |
| `Discount.value` | number |  |
| `Estimation.value` | date |  |
| `id` | string |  |
| `LastModifiedDateTime.value` | date |  |
| `Location.value` | string |  |
| `ManualAmount.value` | boolean |  |
| `NoteID.value` | string |  |
| `OpportunityID.value` | string |  |
| `Override.value` | boolean |  |
| `Project.value` | string |  |
| `Reason.value` | string |  |
| `rowNumber` | number |  |
| `Source.value` | string |  |
| `Stage.value` | string |  |
| `Status.value` | string |  |
| `Subject.value` | string |  |
| `Total.value` | number |  |
| `WeightTotal.value` | number |  |

## Native endpoint

Through the native Acumatica API, this operation is `PUT /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Opportunity` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-opportunity.md) for the provider-specific parameters and requirements.

