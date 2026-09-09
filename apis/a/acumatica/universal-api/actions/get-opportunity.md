# Acumatica: Get Opportunity



```
GET https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-opportunity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-opportunity?connectionId=$CONNECTION_ID&id=041a3b2c-d87f-e411-beca-00b56d0561c2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "041a3b2c-d87f-e411-beca-00b56d0561c2"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-opportunity?${params}`, {
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
| `id` | string | yes | The Acumatica entity ID (GUID) returned in the record's id field. Example: `041a3b2c-d87f-e411-beca-00b56d0561c2`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `select` | string | no | Comma-separated entity fields to return. Example: `OpportunityID,Subject,Status,BusinessAccount`. |
| `expand` | string | no | Comma-separated detail or linked entities to expand. Example: `Contact,Products`. |
| `custom` | string | no | Comma-separated custom fields to return. Example: `OpportunityID,Subject`. |

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
      "CurrencyID": {
        "value": "string"
      },
      "CurrencyViewState": {
        "value": true
      },
      "Details": {
        "value": "string"
      },
      "Discount": {
        "value": 1
      },
      "Estimation": {
        "value": "string"
      },
      "id": "string",
      "LastModifiedDateTime": {
        "value": "string"
      },
      "Location": {
        "value": "string"
      },
      "ManualAmount": {
        "value": true
      },
      "note": {
        "value": "string"
      },
      "NoteID": {
        "value": "string"
      },
      "OpportunityID": {
        "value": "string"
      },
      "Owner": {
        "value": "string"
      },
      "OwnerEmployeeName": {
        "value": "Ava Chen"
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
      "SourceCampaign": {
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
      },
      "WorkgroupDescription": {
        "value": "string"
      },
      "WorkgroupID": {
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
| `Amount.value` | number |  |
| `Branch.value` | string |  |
| `BusinessAccount.value` | string |  |
| `ClassID.value` | string |  |
| `CurrencyID.value` | string |  |
| `CurrencyViewState.value` | boolean |  |
| `Details.value` | string |  |
| `Discount.value` | number |  |
| `Estimation.value` | string |  |
| `id` | string |  |
| `LastModifiedDateTime.value` | string |  |
| `Location.value` | string |  |
| `ManualAmount.value` | boolean |  |
| `note.value` | string |  |
| `NoteID.value` | string |  |
| `OpportunityID.value` | string |  |
| `Owner.value` | string |  |
| `OwnerEmployeeName.value` | string |  |
| `Project.value` | string |  |
| `Reason.value` | string |  |
| `rowNumber` | number |  |
| `Source.value` | string |  |
| `SourceCampaign.value` | string |  |
| `Stage.value` | string |  |
| `Status.value` | string |  |
| `Subject.value` | string |  |
| `Total.value` | number |  |
| `WeightTotal.value` | number |  |
| `WorkgroupDescription.value` | string |  |
| `WorkgroupID.value` | string |  |

## Native endpoint

Through the native Acumatica API, this operation is `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Opportunity/:id` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-opportunity.md) for the provider-specific parameters and requirements.

