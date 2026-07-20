# HigherGov: List Awardees

Retrieves awardees from HigherGov.

```
GET https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-awardees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HigherGov `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-awardees?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-awardees?${params}`, {
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
| `awardeeKeyParent` | string | no | HigherGov Awardee Key at parent level |
| `cageCode` | string | no | CAGE code |
| `primaryNaics` | string | no | Primary registered NAICS code |
| `registrationLastUpdateDate` | string | no | Date the awardee last updated its SAM registration |
| `uei` | string | no | Unique Entity ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "awardee_key": 1,
      "cage_code": "string",
      "clean_name": "Ava Chen",
      "legal_business_name": "Ava Chen",
      "path": "string",
      "primary_naics": {},
      "uei": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `awardee_key` | number |  |
| `cage_code` | string |  |
| `clean_name` | string |  |
| `legal_business_name` | string |  |
| `path` | string |  |
| `primary_naics` | object |  |
| `uei` | string |  |
| `website` | string |  |

## Native endpoint

Through the native HigherGov API, this operation is `GET /api-external/awardee/` (base URL `https://www.highergov.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-awardees.md) for the provider-specific parameters and requirements.

