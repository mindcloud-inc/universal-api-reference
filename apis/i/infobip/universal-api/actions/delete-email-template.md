# Infobip: Delete Email Template



```
DELETE https://connect.mindcloud.co/v1/universal/infobip/latest/actions/delete-email-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infobip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/infobip/latest/actions/delete-email-template?connectionId=$CONNECTION_ID&templateId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/infobip/latest/actions/delete-email-template?${params}`, {
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
| `templateId` | number | yes | Unique identifier (ID) of the email template. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Infobip API returns.

## Native endpoint

Through the native Infobip API, this operation is `DELETE /email/1/templates/{templateId}` (base URL `https://rkpzwe.api.infobip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-email-template.md) for the provider-specific parameters and requirements.

