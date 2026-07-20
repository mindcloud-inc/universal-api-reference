# Agile CRM: Delete Deal

Deletes an existing deal from Agile CRM.

```
DELETE https://connect.mindcloud.co/v1/universal/agileCRM/latest/actions/delete-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agile CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/agileCRM/latest/actions/delete-deal?connectionId=$CONNECTION_ID&dealId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dealId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agileCRM/latest/actions/delete-deal?${params}`, {
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
| `dealId` | list<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dealId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dealId` | string | Deleted deal identifier. |

## Native endpoint

Through the native Agile CRM API, this operation is `DELETE /opportunity/:dealId` (base URL `https://mindcloud.agilecrm.com/dev/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-deal.md) for the provider-specific parameters and requirements.

