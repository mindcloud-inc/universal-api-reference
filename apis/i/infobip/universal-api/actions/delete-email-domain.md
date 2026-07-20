# Infobip: Delete Email Domain



```
DELETE https://connect.mindcloud.co/v1/universal/infobip/latest/actions/delete-email-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infobip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/infobip/latest/actions/delete-email-domain?connectionId=$CONNECTION_ID&domainName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domainName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/infobip/latest/actions/delete-email-domain?${params}`, {
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
| `domainName` | string | yes | Domain name which needs to be deleted. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Infobip API returns.

## Native endpoint

Through the native Infobip API, this operation is `DELETE /email/1/domains/{domainName}` (base URL `https://rkpzwe.api.infobip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-email-domain.md) for the provider-specific parameters and requirements.

