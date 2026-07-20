# Leadfox: Get Contact History



```
GET https://connect.mindcloud.co/v1/universal/leadfox/latest/actions/get-contact-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadfox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadfox/latest/actions/get-contact-history?connectionId=$CONNECTION_ID&email=person%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "person@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadfox/latest/actions/get-contact-history?${params}`, {
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
| `email` | string | yes | Contact email address (mandatory). Example: `person@example.com`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Leadfox API returns.

## Native endpoint

Through the native Leadfox API, this operation is `POST /contact/gethistory/` (base URL `https://app.leadfox.co/service`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-history.md) for the provider-specific parameters and requirements.

