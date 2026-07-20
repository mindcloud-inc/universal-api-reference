# Teamgate: Update Lead

Updates a lead in Teamgate.

```
PUT https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/update-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamgate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/update-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "leadId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/update-lead', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "leadId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `leadId` | string | yes | Lead ID to update. |
| `name` | string | no | Updated lead name. |
| `starred` | string | no | Whether the lead is starred. Use Teamgate values like yes or no. |
| `status` | string | no | Updated lead status name. |
| `industry` | string | no | Updated lead industry name. |
| `tags` | string | no | Updated lead tags. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ownerId` | string | no | Updated owner user ID. |
| `statusDescription` | string | no | Updated lead status description. |
| `sourceId` | string | no | Updated lead source ID. |
| `sourceDescription` | string | no | Updated lead source description. |
| `industryDescription` | string | no | Updated lead industry description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        {}
      ],
      "company": {},
      "created": {},
      "emails": [
        {}
      ],
      "id": 1,
      "industry": {},
      "isDeleted": "string",
      "name": "Ava Chen",
      "owner": {},
      "phones": [
        {}
      ],
      "picture": {},
      "score": {},
      "source": {},
      "starred": "string",
      "status": {},
      "updated": {},
      "urls": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses` | array<object> |  |
| `company` | object |  |
| `created` | object |  |
| `emails` | array<object> |  |
| `id` | number |  |
| `industry` | object |  |
| `isDeleted` | string |  |
| `name` | string |  |
| `owner` | object |  |
| `phones` | array<object> |  |
| `picture` | object |  |
| `score` | object |  |
| `source` | object |  |
| `starred` | string |  |
| `status` | object |  |
| `updated` | object |  |
| `urls` | array<object> |  |

## Native endpoint

Through the native Teamgate API, this operation is `PUT /leads/{{leadId}}` (base URL `https://api.teamgate.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-lead.md) for the provider-specific parameters and requirements.

