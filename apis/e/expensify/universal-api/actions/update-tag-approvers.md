# Expensify: Update Tag Approvers

Updates tag approvers in Expensify.

```
PUT https://connect.mindcloud.co/v1/universal/expensify/latest/actions/update-tag-approvers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Expensify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/expensify/latest/actions/update-tag-approvers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "policyId": "string",
  "tagApproversJson": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/expensify/latest/actions/update-tag-approvers', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "policyId": "string",
    "tagApproversJson": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `policyId` | string | yes | The Expensify policy ID to update. |
| `tagApproversJson` | string | yes | JSON array of tag approver assignments. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "responseCode": 1,
      "responseMessage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `responseCode` | number |  |
| `responseMessage` | string |  |

## Native endpoint

Through the native Expensify API, this operation is `POST ExpensifyIntegrations` (base URL `https://integrations.expensify.com/Integration-Server/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-tag-approvers.md) for the provider-specific parameters and requirements.

