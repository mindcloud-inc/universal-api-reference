# Documentum: Get Audit Trail Relative Date Facets



```
GET https://connect.mindcloud.co/v1/universal/documentum/latest/actions/get-audit-trail-relative-date-facets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documentum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documentum/latest/actions/get-audit-trail-relative-date-facets?connectionId=$CONNECTION_ID&repositoryName=d2repo&objectId=090000018000abcd" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "repositoryName": "d2repo",
  "objectId": "090000018000abcd"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documentum/latest/actions/get-audit-trail-relative-date-facets?${params}`, {
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
| `repositoryName` | string | yes | Documentum repository name. Example: `d2repo`. |
| `objectId` | string | yes | Documentum object ID whose audit facets should be returned. Example: `090000018000abcd`. |
| `eventSource` | string | no | Audit event source: Automatic, Manual, or All. Defaults to All. Default: `All`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "endDate": "2026-05-07T12:00:00.000Z",
      "startDate": "2026-05-07T12:00:00.000Z",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Audit count for the facet. |
| `endDate` | date | Facet end date. |
| `startDate` | date | Facet start date. |
| `title` | string | Relative date facet label. |

## Native endpoint

Through the native Documentum API, this operation is `GET /repositories/{repositoryName}/objects/{objectId}/audit-trail-facets-by-relative-date` (base URL `{{credentials.documentumRestBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-audit-trail-relative-date-facets.md) for the provider-specific parameters and requirements.

