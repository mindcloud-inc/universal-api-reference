# Anyleads: Find Emails By Name And Domain

Finds emails in Anyleads by name and domain.

```
GET https://connect.mindcloud.co/v1/universal/anyleads/latest/actions/find-emails-by-name-and-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anyleads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anyleads/latest/actions/find-emails-by-name-and-domain?connectionId=$CONNECTION_ID&domain=string&firstName=Ava&lastName=Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string",
  "firstName": "Ava",
  "lastName": "Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anyleads/latest/actions/find-emails-by-name-and-domain?${params}`, {
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
| `domain` | string | yes | Company domain to use when generating the likely email. |
| `firstName` | string | yes | Lead first name. |
| `lastName` | string | yes | Lead last name. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Anyleads API returns.

## Native endpoint

Through the native Anyleads API, this operation is `POST /api-product/incoming-webhook/find-emails-first-last` (base URL `https://myapiconnect.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-emails-by-name-and-domain.md) for the provider-specific parameters and requirements.

