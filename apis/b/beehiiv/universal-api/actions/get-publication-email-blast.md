# Beehiiv: Get Publication Email Blast

Retrieves an email blast for a publication from Beehiiv.

```
GET https://connect.mindcloud.co/v1/universal/beehiiv/latest/actions/get-publication-email-blast
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beehiiv `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beehiiv/latest/actions/get-publication-email-blast?connectionId=$CONNECTION_ID&publicationId=string&emailBlastId=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "publicationId": "string",
  "emailBlastId": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beehiiv/latest/actions/get-publication-email-blast?${params}`, {
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
| `publicationId` | string | yes | The prefixed ID of the publication object. |
| `emailBlastId` | string | yes | The prefixed ID of the email blast object. |
| `expand[]` | array<string> | no | Optional list of expandable objects. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Beehiiv API returns.

## Native endpoint

Through the native Beehiiv API, this operation is `GET /v2/publications/:publicationId/email_blasts/:emailBlastId` (base URL `https://api.beehiiv.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-publication-email-blast.md) for the provider-specific parameters and requirements.

