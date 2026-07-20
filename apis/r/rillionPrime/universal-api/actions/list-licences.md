# Rillion Prime: List Licences



```
GET https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-licences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-licences?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-licences?${params}`, {
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
| `licenceId` | number | no | Optional query value for LicenceId. |
| `licence` | string | no | Optional query value for Licence. |
| `isValid` | boolean | no | Optional query value for IsValid. |
| `isActive` | boolean | no | Optional query value for IsActive. |
| `type` | number | no | Optional query value for Type. |
| `nextReportingTime` | date | no | Optional query value for NextReportingTime. |
| `dateCreated` | date | no | Optional query value for DateCreated. |
| `licencee` | string | no | Optional query value for Licencee. |
| `licenceKey` | string | no | Optional query value for LicenceKey. |
| `licenceNo` | string | no | Optional query value for LicenceNo. |
| `environment` | string | no | Optional query value for Environment. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime API returns.

## Native endpoint

Through the native Rillion Prime API, this operation is `GET /licence` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-licences.md) for the provider-specific parameters and requirements.

