# Simplicate: List Sales



```
GET https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/list-sales
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplicate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/list-sales?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/list-sales?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "chanceToScore": 1,
      "contact": {
        "familyName": "Ava Chen",
        "familyNamePrefix": "Ava Chen",
        "firstName": "Ava",
        "id": "string",
        "personId": "string",
        "workEmail": "ava@example.com",
        "workMobile": "string"
      },
      "contactId": "string",
      "created": "string",
      "createdAt": "string",
      "expectedClosingDate": "string",
      "expectedRevenue": 1,
      "id": "string",
      "modified": "string",
      "myOrganizationProfileId": "string",
      "organization": {
        "id": "string",
        "name": "Ava Chen"
      },
      "organizationId": "string",
      "progress": {
        "chanceToScore": 1,
        "color": "string",
        "id": "string",
        "label": "string",
        "position": 1
      },
      "reason": {
        "id": "string",
        "name": "Ava Chen"
      },
      "responsibleEmployee": {
        "id": "string",
        "name": "Ava Chen",
        "personId": "string"
      },
      "separateInvoiceRecipient": {
        "isSeparateInvoiceRecipient": true
      },
      "simplicateUrl": "https://example.com",
      "source": {
        "id": "string",
        "name": "Ava Chen"
      },
      "startDate": "string",
      "status": {
        "id": "string",
        "label": "string"
      },
      "statusUpdatedAt": "string",
      "subject": "string",
      "timelineEmailAddress": "ava@example.com",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chanceToScore` | number |  |
| `contact.familyName` | string |  |
| `contact.familyNamePrefix` | string |  |
| `contact.firstName` | string |  |
| `contact.id` | string |  |
| `contact.personId` | string |  |
| `contact.workEmail` | string |  |
| `contact.workMobile` | string |  |
| `contactId` | string |  |
| `created` | string |  |
| `createdAt` | string |  |
| `expectedClosingDate` | string |  |
| `expectedRevenue` | number |  |
| `id` | string |  |
| `modified` | string |  |
| `myOrganizationProfileId` | string |  |
| `organization.id` | string |  |
| `organization.name` | string |  |
| `organizationId` | string |  |
| `progress.chanceToScore` | number |  |
| `progress.color` | string |  |
| `progress.id` | string |  |
| `progress.label` | string |  |
| `progress.position` | number |  |
| `reason.id` | string |  |
| `reason.name` | string |  |
| `responsibleEmployee.id` | string |  |
| `responsibleEmployee.name` | string |  |
| `responsibleEmployee.personId` | string |  |
| `separateInvoiceRecipient.isSeparateInvoiceRecipient` | boolean |  |
| `simplicateUrl` | string |  |
| `source.id` | string |  |
| `source.name` | string |  |
| `startDate` | string |  |
| `status.id` | string |  |
| `status.label` | string |  |
| `statusUpdatedAt` | string |  |
| `subject` | string |  |
| `timelineEmailAddress` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Simplicate API, this operation is `GET /sales/sales` (base URL `https://{{credentials.subdomain}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sales.md) for the provider-specific parameters and requirements.

