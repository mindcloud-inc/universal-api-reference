# Prospeo: Enrich Person with Verified Email Only

Retrieves enriched person data from Prospeo with verified email only.

```
GET https://connect.mindcloud.co/v1/universal/prospeo/latest/actions/enrich-person-with-verified-email-only
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prospeo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prospeo/latest/actions/enrich-person-with-verified-email-only?connectionId=$CONNECTION_ID&data=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "data": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prospeo/latest/actions/enrich-person-with-verified-email-only?${params}`, {
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
| `data` | object | yes | Person datapoints used for matching. Default: `{"full_name":"Satya Nadella","company_website":"microsoft.com"}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": {},
      "freeEnrichment": true,
      "person": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | object |  |
| `freeEnrichment` | boolean |  |
| `person` | object |  |

## Native endpoint

Through the native Prospeo API, this operation is `POST /enrich-person` (base URL `https://api.prospeo.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enrich-person-with-verified-email-only.md) for the provider-specific parameters and requirements.

