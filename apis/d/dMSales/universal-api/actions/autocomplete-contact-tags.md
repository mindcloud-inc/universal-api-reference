# DMSales: Autocomplete Contact Tags

Finds contact tags in DMSales by partial tag.

```
GET https://connect.mindcloud.co/v1/universal/dMSales/latest/actions/autocomplete-contact-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DMSales `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dMSales/latest/actions/autocomplete-contact-tags?connectionId=$CONNECTION_ID&partTag=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "partTag": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dMSales/latest/actions/autocomplete-contact-tags?${params}`, {
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
| `partTag` | string | yes | Partial tag text to autocomplete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native DMSales API, this operation is `GET /api/contact-card/autocomplete-tags` (base URL `https://app.dmsales.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/autocomplete-contact-tags.md) for the provider-specific parameters and requirements.

