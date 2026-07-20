# Rijksoverheid: Get School Holidays By School Year

Retrieves school holidays for a school year from Rijksoverheid.

```
GET https://connect.mindcloud.co/v1/universal/rijksoverheid/latest/actions/get-school-holidays-by-school-year
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rijksoverheid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rijksoverheid/latest/actions/get-school-holidays-by-school-year?connectionId=$CONNECTION_ID&schoolYear=2029-2030" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "schoolYear": "2029-2030"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rijksoverheid/latest/actions/get-school-holidays-by-school-year?${params}`, {
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
| `schoolYear` | string | yes | School year to retrieve in YYYY-YYYY format, for example 2029-2030. Default: `2029-2030`. Example: `2029-2030`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorities": [
        "string"
      ],
      "canonical": "string",
      "content": [
        {}
      ],
      "creators": [
        "string"
      ],
      "id": "string",
      "language": "string",
      "lastmodified": "2026-05-07T12:00:00.000Z",
      "license": "string",
      "location": "string",
      "notice": "string",
      "rightsholders": [
        "string"
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorities` | array<string> | Responsible government authority names. |
| `canonical` | string | Canonical Rijksoverheid page URL for the requested school-year holiday overview. |
| `content` | array<object> | School-year holiday content, including title, school year, and vacation periods. |
| `creators` | array<string> | Creator organization names. |
| `id` | string | Unique identifier for the school holiday data record. |
| `language` | string | Language tag for the response data. |
| `lastmodified` | date | Last modified timestamp for the record. |
| `license` | string | Reuse license for the data. |
| `location` | string | Geographic location for the data. |
| `notice` | string | Additional notice text from Rijksoverheid about advisory or compulsory dates. |
| `rightsholders` | array<string> | Organizations that hold or manage the rights. |
| `type` | string | Information type returned by Rijksoverheid. |

## Native endpoint

Through the native Rijksoverheid API, this operation is `GET /v1/infotypes/schoolholidays/schoolyear/{{schoolYear}}` (base URL `https://opendata.rijksoverheid.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-school-holidays-by-school-year.md) for the provider-specific parameters and requirements.

