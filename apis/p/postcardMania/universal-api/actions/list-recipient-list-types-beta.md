# PostcardMania: List Recipient List Types (Beta)

Retrieves beta recipient list types from PostcardMania.

```
GET https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/list-recipient-list-types-beta
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostcardMania `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/list-recipient-list-types-beta?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/list-recipient-list-types-beta?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "key": "string",
      "label": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `key` | string | Provider key for the PostcardMania list type. |
| `label` | string | Human-readable label for the PostcardMania list type. |

## Native endpoint

Through the native PostcardMania API, this operation is `GET /list/types` (base URL `https://v3.pcmintegrations.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-recipient-list-types-beta.md) for the provider-specific parameters and requirements.

