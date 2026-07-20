# Dynosend: Get Contact by UID

Retrieves a contact from Dynosend by UID.

```
GET https://connect.mindcloud.co/v1/universal/dynosend/latest/actions/get-contact-by-uid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dynosend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dynosend/latest/actions/get-contact-by-uid?connectionId=$CONNECTION_ID&audienceUid=string&contactUid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "audienceUid": "string",
  "contactUid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dynosend/latest/actions/get-contact-by-uid?${params}`, {
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
| `audienceUid` | string | yes | The UID of the audience that contains the contact. |
| `contactUid` | string | yes | The UID of the contact to fetch. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dynosend API returns.

## Native endpoint

Through the native Dynosend API, this operation is `GET /contacts` (base URL `https://api.dynosend.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-by-uid.md) for the provider-specific parameters and requirements.

