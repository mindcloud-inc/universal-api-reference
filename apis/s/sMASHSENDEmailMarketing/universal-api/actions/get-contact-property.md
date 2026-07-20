# SMASHSEND Email Marketing: Get Contact Property

Retrieves a contact property by ID from SMASHSEND.

```
GET https://connect.mindcloud.co/v1/universal/sMASHSENDEmailMarketing/latest/actions/get-contact-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMASHSEND Email Marketing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMASHSENDEmailMarketing/latest/actions/get-contact-property?connectionId=$CONNECTION_ID&propertyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "propertyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMASHSENDEmailMarketing/latest/actions/get-contact-property?${params}`, {
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
| `propertyId` | string | yes | The SMASHSEND contact property ID to retrieve. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SMASHSEND Email Marketing API returns.

## Native endpoint

Through the native SMASHSEND Email Marketing API, this operation is `GET /v1/contact-properties/:propertyId` (base URL `https://api.smashsend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-property.md) for the provider-specific parameters and requirements.

