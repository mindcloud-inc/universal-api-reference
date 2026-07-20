# Simplicate: Get Sale



```
GET https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/get-sale
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplicate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/get-sale?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/get-sale?${params}`, {
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
| `id` | string | yes | The sale id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chanceToScore": 1,
      "created": "string",
      "createdAt": "string",
      "id": "string",
      "modified": "string",
      "myOrganizationProfileId": "string",
      "note": "string",
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
      "separateInvoiceRecipient": {
        "isSeparateInvoiceRecipient": true
      },
      "simplicateUrl": "https://example.com",
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
| `created` | string |  |
| `createdAt` | string |  |
| `id` | string |  |
| `modified` | string |  |
| `myOrganizationProfileId` | string |  |
| `note` | string |  |
| `organization.id` | string |  |
| `organization.name` | string |  |
| `organizationId` | string |  |
| `progress.chanceToScore` | number |  |
| `progress.color` | string |  |
| `progress.id` | string |  |
| `progress.label` | string |  |
| `progress.position` | number |  |
| `separateInvoiceRecipient.isSeparateInvoiceRecipient` | boolean |  |
| `simplicateUrl` | string |  |
| `startDate` | string |  |
| `status.id` | string |  |
| `status.label` | string |  |
| `statusUpdatedAt` | string |  |
| `subject` | string |  |
| `timelineEmailAddress` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Simplicate API, this operation is `GET /sales/sales/:id` (base URL `https://{{credentials.subdomain}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sale.md) for the provider-specific parameters and requirements.

