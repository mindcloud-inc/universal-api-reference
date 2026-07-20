# Toofr: Guess Email

Guesses a prospect's email address in Toofr.

```
GET https://connect.mindcloud.co/v1/universal/toofr/latest/actions/guess-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toofr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/toofr/latest/actions/guess-email?connectionId=$CONNECTION_ID&companyName=Ava%20Chen&firstName=Ava&lastName=Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyName": "Ava Chen",
  "firstName": "Ava",
  "lastName": "Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/toofr/latest/actions/guess-email?${params}`, {
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
| `companyName` | string | yes | Person company name or domain. |
| `firstName` | string | yes | Person first name. |
| `lastName` | string | yes | Person last name. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Toofr API returns.

## Native endpoint

Through the native Toofr API, this operation is `POST /guess_email.json` (base URL `https://www.findemails.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/guess-email.md) for the provider-specific parameters and requirements.

