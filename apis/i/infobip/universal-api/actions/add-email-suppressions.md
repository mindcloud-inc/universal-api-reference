# Infobip: Add Email Suppressions



```
POST https://connect.mindcloud.co/v1/universal/infobip/latest/actions/add-email-suppressions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infobip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/infobip/latest/actions/add-email-suppressions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "suppressions": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/infobip/latest/actions/add-email-suppressions', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "suppressions": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `suppressions` | list<object> | yes | Email addresses to add to the suppression list. Number of destinations cannot exceed 10,000. |
| `suppressions.domainName` | string | no | Domain name from which suppressions will be added. |
| `suppressions.emailAddress` | list<string> | no | Email addresses to add to suppression list. |
| `suppressions.type` | string | no | Type of suppression. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Infobip API returns.

## Native endpoint

Through the native Infobip API, this operation is `POST /email/1/suppressions` (base URL `https://rkpzwe.api.infobip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-email-suppressions.md) for the provider-specific parameters and requirements.

