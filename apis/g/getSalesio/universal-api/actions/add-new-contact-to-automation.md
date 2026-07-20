# GetSales.io: Add New Contact To Automation



```
POST https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/add-new-contact-to-automation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GetSales.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/add-new-contact-to-automation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "flowUuid": "string",
  "lead.linkedinId": "john-doe-123456",
  "listUuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/add-new-contact-to-automation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "flowUuid": "string",
    "lead.linkedinId": "john-doe-123456",
    "listUuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `flowUuid` | string | yes | UUID of the automation to add the new contact to. |
| `lead.linkedinId` | string | yes | Contact LinkedIn ID or profile handle. Example: `john-doe-123456`. |
| `lead.firstName` | string | no | Contact first name. Example: `John`. |
| `lead.lastName` | string | no | Contact last name. Example: `Doe`. |
| `lead.companyName` | string | no | Contact company name. Example: `ExampleCorp`. |
| `lead.email` | string | no | Contactable email address for the contact. Example: `john.doe@example.com`. |
| `listUuid` | string | yes | UUID of the target list. |
| `flowSegmentId` | number | no | ID of a specific automation segment. Defaults to 1 when omitted. Default: `1`. |
| `skipIfLeadExists` | boolean | no | When true, existing contacts are not added to the automation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "lead": {},
      "message": "string",
      "reason": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `lead` | object |  |
| `message` | string |  |
| `reason` | string |  |

## Native endpoint

Through the native GetSales.io API, this operation is `POST /flows/api/flows/{flowUuid}/add-new-lead` (base URL `https://amazing.getsales.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-new-contact-to-automation.md) for the provider-specific parameters and requirements.

