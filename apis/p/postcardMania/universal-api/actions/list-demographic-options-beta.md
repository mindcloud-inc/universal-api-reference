# PostcardMania: List Demographic Options (Beta)

Retrieves beta demographic options from PostcardMania.

```
GET https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/list-demographic-options-beta
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostcardMania `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/list-demographic-options-beta?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/list-demographic-options-beta?${params}`, {
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
| `listType` | string | no | Recipient list type key from Get List Types (BETA). Example: IRL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "key": "string",
      "label": "string",
      "values": [
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
| `key` | string | Provider key for the demographic option. |
| `label` | string | Human-readable label for the demographic option. |
| `values` | array<object> | Selectable values for the demographic option. |

## Native endpoint

Through the native PostcardMania API, this operation is `GET /list/demographics` (base URL `https://v3.pcmintegrations.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-demographic-options-beta.md) for the provider-specific parameters and requirements.

