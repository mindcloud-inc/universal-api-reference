# Synthflow AI Phone Calling: Get Phone Number

Retrieves a phone number from Synthflow.

```
GET https://connect.mindcloud.co/v1/universal/synthflowAIPhoneCalling/latest/actions/get-phone-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Synthflow AI Phone Calling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/synthflowAIPhoneCalling/latest/actions/get-phone-number?connectionId=$CONNECTION_ID&phoneNumberSlug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "phoneNumberSlug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/synthflowAIPhoneCalling/latest/actions/get-phone-number?${params}`, {
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
| `phoneNumberSlug` | string | yes | The phone number slug without the leading plus sign. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Synthflow AI Phone Calling API returns.

## Native endpoint

Through the native Synthflow AI Phone Calling API, this operation is `GET /numbers/:phone_number_slug` (base URL `https://api.synthflow.ai/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-phone-number.md) for the provider-specific parameters and requirements.

