# DailyMed: List SPLs

Retrieves SPLs from DailyMed.

```
GET https://connect.mindcloud.co/v1/universal/dailyMed/latest/actions/list-spls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DailyMed `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dailyMed/latest/actions/list-spls?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dailyMed/latest/actions/list-spls?${params}`, {
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
| `drugName` | string | no | Generic or brand name to search for. |
| `ndc` | string | no | National Drug Code to search for. |
| `rxcui` | string | no | RxNorm Concept Unique Identifier. |
| `setid` | string | no | Set ID of a label. Default: `4543e156-1deb-666e-e063-6394a90a719c`. |
| `applicationNumber` | string | no | New Drug Application number. |
| `publishedDate` | date | no | DailyMed published date in YYYY-MM-DD format. |
| `publishedDateComparison` | string | no | Comparison for the published date: lt, lte, gt, gte, or eq. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `nameType` | string | no | Whether the drug name is generic, brand, or both. |
| `boxedWarning` | boolean | no | Whether the drug contains a boxed warning: true or false. |
| `deaScheduleCode` | string | no | DEA schedule code, such as none, C48672, C48675, C48676, C48677, or C48679. |
| `doctype` | string | no | FDA LOINC document/content type code for the label. |
| `drugClassCode` | string | no | Pharmacologic drug class code. |
| `drugClassCodingSystem` | string | no | Coding system for the drug class code. |
| `labeler` | string | no | Name of the labeler for the drug. |
| `manufacturer` | string | no | Name of the manufacturer for the drug. |
| `marketingCategoryCode` | string | no | FDA marketing category code. |
| `uniiCode` | string | no | Unique Ingredient Identifier code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "published_date": "2026-05-07T12:00:00.000Z",
      "setid": "string",
      "spl_version": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `published_date` | date | Date the label was published on DailyMed. |
| `setid` | string | SPL Set ID. |
| `spl_version` | number | SPL version number. |
| `title` | string | SPL title. |

## Native endpoint

Through the native DailyMed API, this operation is `GET /spls.json` (base URL `https://dailymed.nlm.nih.gov/dailymed/services/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-spls.md) for the provider-specific parameters and requirements.

