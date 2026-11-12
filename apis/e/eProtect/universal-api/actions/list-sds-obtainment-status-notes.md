# 3E Protect: List SDS Obtainment Status Notes



```
GET https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/list-sds-obtainment-status-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 3E Protect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/list-sds-obtainment-status-notes?connectionId=$CONNECTION_ID&source=string&identifier=string&locale=en&country=USA&startDate=YYYY-MM-DD" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "source": "string",
  "identifier": "string",
  "locale": "en",
  "country": "USA",
  "startDate": "YYYY-MM-DD"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/list-sds-obtainment-status-notes?${params}`, {
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
| `source` | string | yes | Exact, case-sensitive product identifier source name agreed with 3E. |
| `identifier` | string | yes | Your product identifier value for the selected source. |
| `locale` | string | yes | Two-letter language code, such as en. Use a language configured in List SDS Requirements. Example: `en`. |
| `country` | string | yes | Three-letter country code, such as USA. Use a country configured in List SDS Requirements. Example: `USA`. |
| `startDate` | date | yes | Include status changes since this date. Sent as YYYY-MM-DD. Example: `YYYY-MM-DD`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 3E Protect API returns.

## Native endpoint

Through the native 3E Protect API, this operation is `GET /catalog-item-obtainment-status-notes/:source/:identifier/:locale/:country` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sds-obtainment-status-notes.md) for the provider-specific parameters and requirements.

