# UKG Pro: Get Employee Employment Details



```
GET https://connect.mindcloud.co/v1/universal/ukgPro/latest/actions/get-employee-employment-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UKG Pro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ukgPro/latest/actions/get-employee-employment-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ukgPro/latest/actions/get-employee-employment-details?${params}`, {
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
| `primaryJobCode` | string | no |  |
| `payGroup` | string | no |  |
| `employeeStatusCode` | string | no |  |
| `dateTimeChanged` | string | no |  |
| `employeeId` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native UKG Pro API returns.

## Native endpoint

Through the native UKG Pro API, this operation is `GET personnel/v1/employee-employment-details` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-employee-employment-details.md) for the provider-specific parameters and requirements.

