# Poper: List Popup Responses

Retrieves responses for a specific Poper popup.

```
GET https://connect.mindcloud.co/v1/universal/poper/latest/actions/list-popup-responses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Poper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/poper/latest/actions/list-popup-responses?connectionId=$CONNECTION_ID&popup_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "popup_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/poper/latest/actions/list-popup-responses?${params}`, {
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
| `popup_id` | string | yes | The popup identifier whose responses you want to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "responses": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `responses` | array<object> | Array of popup response records for the selected popup. |

## Native endpoint

Through the native Poper API, this operation is `POST /popup/responses` (base URL `https://api.poper.ai/general/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-popup-responses.md) for the provider-specific parameters and requirements.

