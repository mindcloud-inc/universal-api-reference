# Finnish BIS: List Post Codes

Retrieves postal code details from Finnish BIS.

```
GET https://connect.mindcloud.co/v1/universal/finnishBIS/latest/actions/list-post-codes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finnish BIS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnishBIS/latest/actions/list-post-codes?connectionId=$CONNECTION_ID&lang=en" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lang": "en"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finnishBIS/latest/actions/list-post-codes?${params}`, {
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
| `lang` | list<string> | yes | Language code for postal code details. One of: `en`, `fi`, `sv`. Default: `en`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "city": "string",
      "languageCode": "string",
      "municipalityCode": "string",
      "postCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | Whether the post code is active. |
| `city` | string | Postal city or destination name. |
| `languageCode` | string | Language code used by the source record. |
| `municipalityCode` | string | Finnish municipality code. |
| `postCode` | string | Finnish postal code. |

## Native endpoint

Through the native Finnish BIS API, this operation is `GET /post_codes` (base URL `https://avoindata.prh.fi/opendata-ytj-api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-post-codes.md) for the provider-specific parameters and requirements.

