# leadtributor.cloud: List Leads

Retrieves leads owned by your company in leadtributor.cloud.

```
GET https://connect.mindcloud.co/v1/universal/leadtributorcloud/latest/actions/list-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a leadtributor.cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadtributorcloud/latest/actions/list-leads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadtributorcloud/latest/actions/list-leads?${params}`, {
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
| `commission.closedAt` | string | no | Filter leads by commission.closedAt using the provider filter syntax. |
| `commission.responsible` | string | no | Filter leads by commission.responsible. |
| `commission.startedAt` | string | no | Filter leads by commission.startedAt using the provider filter syntax. |
| `continuation` | string | no | Continuation token for the next page of leads. |
| `includeFieldLists` | boolean | no | Whether to include lead field lists in the response. |
| `lead.createdAt` | string | no | Filter leads by lead.createdAt using the provider filter syntax. |
| `maxResults` | number | no | Maximum number of leads to return. Default: `100`. |
| `modifiedAt` | string | no | Filter leads by modifiedAt using the provider filter syntax. |
| `sort` | string | no | Sort expression for the leads list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commission": {
        "closedAt": "string",
        "commissionId": "string",
        "outcome": "string",
        "responsible": "string",
        "startedAt": "string",
        "step": 1
      },
      "lead": {
        "createdAt": "string",
        "leadId": "string",
        "modifiedAt": "string",
        "owner": "string",
        "serial": 1
      },
      "modifiedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commission.closedAt` | string | Commission closed timestamp. |
| `commission.commissionId` | string | Commission ID when the lead is commissioned. |
| `commission.outcome` | string | Commission outcome. |
| `commission.responsible` | string | Responsible commission URN. |
| `commission.startedAt` | string | Commission start timestamp. |
| `commission.step` | number | Commission step number. |
| `lead.createdAt` | string | Lead creation timestamp. |
| `lead.leadId` | string | Lead ID. |
| `lead.modifiedAt` | string | Lead modification timestamp. |
| `lead.owner` | string | Lead owner URN. |
| `lead.serial` | number | Lead serial number. |
| `modifiedAt` | string | Last modification timestamp for the lead list item. |

## Native endpoint

Through the native leadtributor.cloud API, this operation is `GET /leads` (base URL `https://api.leadtributor.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-leads.md) for the provider-specific parameters and requirements.

