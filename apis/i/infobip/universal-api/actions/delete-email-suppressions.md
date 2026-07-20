# Infobip: Delete Email Suppressions



```
DELETE https://connect.mindcloud.co/v1/universal/infobip/latest/actions/delete-email-suppressions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infobip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/infobip/latest/actions/delete-email-suppressions?connectionId=$CONNECTION_ID&suppressions=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "suppressions": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/infobip/latest/actions/delete-email-suppressions?${params}`, {
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
| `suppressions` | list<object> | yes | Email addresses to delete from the suppression list. Number of destinations cannot exceed 10,000. |
| `suppressions.domainName` | string | no | Domain name from which suppressions will be deleted. |
| `suppressions.emailAddress` | list<string> | no | Email addresses that need to be deleted. |
| `suppressions.type` | string | no | Type of suppression. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Infobip API returns.

## Native endpoint

Through the native Infobip API, this operation is `DELETE /email/1/suppressions` (base URL `https://rkpzwe.api.infobip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-email-suppressions.md) for the provider-specific parameters and requirements.

