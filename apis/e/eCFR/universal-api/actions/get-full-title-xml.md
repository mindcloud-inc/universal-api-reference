# eCFR: Get Full Title XML

Retrieves the full XML for a title from eCFR.

```
GET https://connect.mindcloud.co/v1/universal/eCFR/latest/actions/get-full-title-xml
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eCFR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eCFR/latest/actions/get-full-title-xml?connectionId=$CONNECTION_ID&date=string&title=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "date": "string",
  "title": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eCFR/latest/actions/get-full-title-xml?${params}`, {
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
| `date` | string | yes | eCFR version date in YYYY-MM-DD format. |
| `title` | number | yes | CFR title number, such as 1. |
| `part` | string | no | Optional CFR part identifier to limit returned XML, such as 1. |
| `section` | string | no | Optional section identifier, such as 1.1. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string | XML content returned by the eCFR full-content endpoint. |

## Native endpoint

Through the native eCFR API, this operation is `GET /api/versioner/v1/full/:date/title-:title.xml` (base URL `https://www.ecfr.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-full-title-xml.md) for the provider-specific parameters and requirements.

