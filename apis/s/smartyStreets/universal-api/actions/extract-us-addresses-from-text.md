# Smarty-streets: Extract US Addresses From Text

Extracts US addresses from text in Smarty-streets.

```
GET https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/extract-us-addresses-from-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smarty-streets `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/extract-us-addresses-from-text?connectionId=$CONNECTION_ID&text=There%20are%20addresses%20everywhere.%201%20Santa%20Claus%20Ln%20North%20Pole%20AK%2099705." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "There are addresses everywhere. 1 Santa Claus Ln North Pole AK 99705."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/extract-us-addresses-from-text?${params}`, {
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
| `text` | string | yes | Text containing addresses to extract. Default: `There are addresses everywhere. 1 Santa Claus Ln North Pole AK 99705. Smarty can find them.`. Example: `There are addresses everywhere. 1 Santa Claus Ln North Pole AK 99705.`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        {}
      ],
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses` | array<object> |  |
| `meta` | object |  |

## Native endpoint

Through the native Smarty-streets API, this operation is `POST https://us-extract.api.smarty.com/` (base URL `https://us-street.api.smarty.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-us-addresses-from-text.md) for the provider-specific parameters and requirements.

