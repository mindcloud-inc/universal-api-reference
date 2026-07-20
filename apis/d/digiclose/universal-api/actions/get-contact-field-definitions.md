# Digiclose: Get Contact Field Definitions



```
GET https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/get-contact-field-definitions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digiclose `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/get-contact-field-definitions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/get-contact-field-definitions?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Digiclose API returns.

## Native endpoint

Through the native Digiclose API, this operation is `GET /contacts/fieldset` (base URL `https://app.digiclose.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-field-definitions.md) for the provider-specific parameters and requirements.

