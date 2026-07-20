# ProPublica Nonprofit Explorer: Get Organization

Retrieves an organization from ProPublica Nonprofit Explorer by EIN.

```
GET https://connect.mindcloud.co/v1/universal/proPublicaNonprofitExplorer/latest/actions/get-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProPublica Nonprofit Explorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proPublicaNonprofitExplorer/latest/actions/get-organization?connectionId=$CONNECTION_ID&ein=142007220" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ein": "142007220"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/proPublicaNonprofitExplorer/latest/actions/get-organization?${params}`, {
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
| `ein` | string | yes | Integer employer identification number for the organization, without a dash. Leading zeroes are trimmed by the API. Example: `142007220`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "api_version": 1,
      "data_source": "string",
      "filings_with_data": [
        {}
      ],
      "filings_without_data": [
        {}
      ],
      "organization": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `api_version` | number | Nonprofit Explorer API version. |
| `data_source` | string | Source citation returned by the API. |
| `filings_with_data` | array<object> | Form 990 filings with extracted data. |
| `filings_without_data` | array<object> | Filing records that only include tax period, PDF URL, and form type. |
| `organization` | object | Profile data for the nonprofit organization. |

## Native endpoint

Through the native ProPublica Nonprofit Explorer API, this operation is `GET /organizations/{{ein}}.json` (base URL `https://projects.propublica.org/nonprofits/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization.md) for the provider-specific parameters and requirements.

