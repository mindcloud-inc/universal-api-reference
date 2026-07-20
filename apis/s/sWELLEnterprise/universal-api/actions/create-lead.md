# SWELLEnterprise: Create Lead

Creates a new lead in SWELLEnterprise.

```
POST https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/create-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SWELLEnterprise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/create-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "statusId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/create-lead', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "statusId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | The lead title. |
| `value` | number | no | The lead value. |
| `statusId` | number | yes | The status ID. |
| `sourceId` | number | no | The referral source ID. |
| `companyId` | number | no | The company ID. |
| `assignedTo` | number | no | The assigned user ID. |
| `description` | string | no | The lead description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "assignedTo": 1,
        "assignedUser": {},
        "company": {
          "id": 1,
          "name": "Ava Chen"
        },
        "companyId": 1,
        "createdAt": "2026-05-07T12:00:00.000Z",
        "deletedAt": "2026-05-07T12:00:00.000Z",
        "description": "string",
        "id": 1,
        "referralSource": {},
        "sourceId": 1,
        "status": {},
        "statusId": 1,
        "title": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "value": "string"
      },
      "message": "string",
      "meta": {
        "timestamp": "2026-05-07T12:00:00.000Z",
        "version": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.assignedTo` | number | The assigned user ID. |
| `data.assignedUser` | object | The assigned user. |
| `data.company.id` | number | The company ID. |
| `data.company.name` | string | The company name. |
| `data.companyId` | number | The linked company ID. |
| `data.createdAt` | date | When the lead was created. |
| `data.deletedAt` | date | When the lead was deleted. |
| `data.description` | string | The lead description. |
| `data.id` | number | The lead ID. |
| `data.referralSource` | object | The referral source. |
| `data.sourceId` | number | The referral source ID. |
| `data.status` | object | The lead status. |
| `data.statusId` | number | The status ID. |
| `data.title` | string | The lead title. |
| `data.updatedAt` | date | When the lead was last updated. |
| `data.value` | string | The lead value. |
| `message` | string | Success message. |
| `meta.timestamp` | date | Response timestamp. |
| `meta.version` | string | API version. |

## Native endpoint

Through the native SWELLEnterprise API, this operation is `POST /crm/leads` (base URL `https://dashboard.swellsystem.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-lead.md) for the provider-specific parameters and requirements.

