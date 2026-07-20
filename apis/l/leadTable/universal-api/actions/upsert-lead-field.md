# LeadTable: Upsert lead field



```
PUT https://connect.mindcloud.co/v1/universal/leadTable/latest/actions/upsert-lead-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LeadTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/leadTable/latest/actions/upsert-lead-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "leadID": "string",
  "question": "string",
  "answer": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leadTable/latest/actions/upsert-lead-field', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "leadID": "string",
    "question": "string",
    "answer": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `leadID` | string | yes | The lead to update. |
| `question` | string | yes | The lead field name to create or update. |
| `answer` | string | yes | The value to store in the selected lead field. |
| `setVisibleInProfile` | boolean | no | Whether the field should be visible in the lead profile. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "lead": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `lead` | object | Updated lead record. |

## Native endpoint

Through the native LeadTable API, this operation is `PUT /lead/{leadID}` (base URL `https://api.lead-table.com/api/v3/external`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-lead-field.md) for the provider-specific parameters and requirements.

