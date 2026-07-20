# ClearoutPhone: Download Bulk Phone Number Validation Result

Retrieves the result of a bulk validation job from ClearoutPhone.

```
GET https://connect.mindcloud.co/v1/universal/clearoutPhone/latest/actions/download-bulk-phone-number-validation-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClearoutPhone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clearoutPhone/latest/actions/download-bulk-phone-number-validation-result?connectionId=$CONNECTION_ID&listId=5d076c8e3b53f9b0f3cf6abb" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "5d076c8e3b53f9b0f3cf6abb"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clearoutPhone/latest/actions/download-bulk-phone-number-validation-result?${params}`, {
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
| `listId` | string | yes | Bulk validation list identifier Example: `5d076c8e3b53f9b0f3cf6abb`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `url` | string |  |

## Native endpoint

Through the native ClearoutPhone API, this operation is `POST /download/result` (base URL `https://api.clearoutphone.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-bulk-phone-number-validation-result.md) for the provider-specific parameters and requirements.

