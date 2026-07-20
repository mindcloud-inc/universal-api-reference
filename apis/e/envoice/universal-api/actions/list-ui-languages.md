# Envoice: List UI Languages

Retrieves supported UI languages from Envoice.

```
GET https://connect.mindcloud.co/v1/universal/envoice/latest/actions/list-ui-languages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Envoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/envoice/latest/actions/list-ui-languages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/envoice/latest/actions/list-ui-languages?${params}`, {
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
      "Id": 1,
      "Name": "Ava Chen",
      "UiCulture": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Id` | number | UI language identifier. |
| `Name` | string | UI language display name. |
| `UiCulture` | string | UI culture code. |

## Native endpoint

Through the native Envoice API, this operation is `GET general/uilanguages` (base URL `https://www.envoice.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-ui-languages.md) for the provider-specific parameters and requirements.

